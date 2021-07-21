- [API 文档](http://poi.apache.org/apidocs/5.0/)
- [example](http://poi.apache.org/components/spreadsheet/examples.html)
## 导出的模板代码
```
    private <T> HSSFWorkbook generateExcel(List<T> datas,Class<T> t) throws NoSuchMethodException, IllegalAccessException, InvocationTargetException {
        HSSFWorkbook excel = createExcel();
        List<String> headers = getHeaders(t);
        setHeader(excel, headers);
        setRowStyle(excel);
        setValue(excel, datas, t);
        return excel;
    }
    
    private <T> List<String> getHeaders(Class<T> t) {
    List<String> headers = new ArrayList<>();
    Field[] fields = t.getDeclaredFields();
    for (Field field : fields) {
        if (field.isAnnotationPresent(Column.class)) {
            headers.add(field.getAnnotation(Column.class).value());
        }
    }
    return headers;
    }
    
    private <T> void setHeader(HSSFWorkbook excel, List<String> headers) {
        HSSFSheet sheet = excel.getSheetAt(0);
        HSSFRow row = sheet.createRow(0);
        for (int i = 0; i < headers.size(); i++) {
            row.createCell(i).setCellValue(headers.get(i));
        }
    }
    
    private <T> void setRowStyle(HSSFWorkbook workbook) {
        HSSFSheet sheet = workbook.getSheetAt(0);
        sheet.setDefaultColumnWidth(20);
    }
    
    private <T> void setValue(HSSFWorkbook excel, List<T> datas, Class<T> t) throws NoSuchMethodException, InvocationTargetException, IllegalAccessException,TypeConstraintException {
        HSSFSheet sheet = excel.getSheetAt(0);
        int rowCount = 1;
        List<Method> methods = new ArrayList<>();
        Field[] fields = t.getDeclaredFields();
        for (Field field : fields) {
            if (field.isAnnotationPresent(Column.class)) {
                String methodName = String.format("get%s",toTitle(field.getName()));
                Method method = t.getMethod(methodName);
                methods.add(method);
            }
        }
        for (T data : datas) {
            HSSFRow row = sheet.createRow(rowCount++);
            int i =0;
            for (Method method : methods) {
                Type type = method.getGenericReturnType();
                if (type.getTypeName().equals("java.lang.Integer")) {
                    Integer value = (Integer) method.invoke(data);
                    row.createCell(i++).setCellValue(value);
                } else if (type.getTypeName().equals("java.lang.String")) {
                    String value = (String) method.invoke(data);
                    row.createCell(i++).setCellValue(value);
                } else {
                    throw new TypeConstraintException("类型错误");
                }
            }
        }
    }
    
    public static String toTitle(String name) {
    char[] chars = name.toCharArray();
    chars[0] -= 32;
    return String.valueOf(chars);

    }
```
```
@Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.FIELD)
@Documented
public @interface Column {
    String value() default "";

}
```

## 导入的模板代码
```
public static <T> List<T> generateDataFromExcel(Sheet sheet, Class<T> clazz) throws InvocationTargetException, IllegalAccessException, NoSuchMethodException, InstantiationException {

        List<Method> methods = new ArrayList<>();
        Field[] fields = clazz.getDeclaredFields();
        for (Field field : fields) {
            if (field.isAnnotationPresent(Column.class)) {
                String methodName = String.format("set%s",toTitle(field.getName()));
                Method method = clazz.getMethod(methodName, field.getType());
                methods.add(method);
            }
        }
        List<T> datas = new ArrayList<>();
        for (int rowCount = 1; rowCount < sheet.getLastRowNum(); rowCount++) {
            Row row = sheet.getRow(rowCount);
            if (row == null) {
                break;
            }
            T t = clazz.newInstance();
            for (int i=0; i< methods.size(); i++) {
                Method method = methods.get(i);
                Type type = method.getParameterTypes()[0];
                Cell cell = row.getCell(i);
                if (cell == null) {
                    continue;
                }
                if (type.getTypeName().equals("java.lang.Integer")) {
                    Double value =  cell.getNumericCellValue();
                    method.invoke(t, value);
                } else if (type.getTypeName().equals("java.lang.String")) {
                    String value =  cell.getStringCellValue();
                    method.invoke(t,value);
                } else if (type.getTypeName().equals("java.util.Date")) {
                    Date value =  cell.getDateCellValue();
                    method.invoke(t,value);
                } else if (type.getTypeName().equals("java.lang.Double")) {
                    Double value =  cell.getNumericCellValue();
                    method.invoke(t,value);
                } else {
                    throw new TypeConstraintException("类型错误");
                }
           }
            datas.add(t);
        }
        return datas;
    }
 ```
