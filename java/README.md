- [正则表达式](re)
- [并发](concurrent)
- [IO](io)
- [容器](collection)
- [虚拟机](jvm)
- [java8 api](https://www.matools.com/api/java8)
- [java新特性](java新特性)
- [Date](date)
- [String](string)
## 软件设计的一些原则
- 接口的解耦，对扩展开发，对修改关闭
- 《23种设计模式》
- TDD
- 敏捷开发
- 重构、代码整洁之道
## 泛型
- private <T> HSSFWorkbook generateExcel(List<T> datas,Class<T> t) {}
## 反射
- 获取对象所有字段上面的注解值[link](https://blog.csdn.net/weixin_41996632/article/details/104266179)
```
List<String> headers = new ArrayList<>();
        Field[] fields = t.getFields();
        for (Field field : fields) {
            if (field.isAnnotationPresent(Column.class)) {
                headers.add(field.getAnnotation(Column.class).value());
            }
        }
```
- getFields()：获得某个类的所有的公共（public）的字段，包括父类中的字段。 
- getDeclaredFields()：获得某个类的所有声明的字段，即包括public、private和proteced，但是不包括父类的申明字段。
- invode对象的方法
```
  method.invoke(data);#data是对象
```
## 注解
- 元注解 @Target @Rententionl
