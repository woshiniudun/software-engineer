## 基本用法
- 获取当月、前x月的第一天和最后一天
```
//获取最后一天
Calendar calendar = Calendar.getInstance();
calendar.set(Calendar.MONTH, - monthBeforeNow + 1);
calendar.add(Calendar.DAY_OF_MONTH, -1);
```
- 日期格式转化字符串 [类的基本用法](http://c.biancheng.net/view/878.html)
```
Date date = new Date();
SimpleDateFormat sdf = new SimpleDateFormat("YY-MM-DD");
String dateStr=sdf.format(date);
```
- 字符串转化日期格式
```
String nowDate = "2021-06-21";
SimpleDateFormat sdf = new SimpleDateFormat("YYYY-MM-DD");
Date date=sdf.parse(nowDate);
```
- 基本的几个类 Date Calender SimpleDateFormat 
- [获取年份、月份、天](https://www.runoob.com/java/date-year-month.html)
```
Calendar cal = Calendar.getInstance();
int day = cal.get(Calendar.DATE);
int month = cal.get(Calendar.MONTH) + 1;
int year = cal.get(Calendar.YEAR);
```
