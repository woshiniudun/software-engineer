## 基本用法
- 获取当月、前x月的第一天和最后一天
```
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
