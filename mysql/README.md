## 增删改查基本用法 [博客](https://www.cnblogs.com/heyangblog/p/7624645.html)
- INSERT INTO 表名（字段名1，字段名2，…）VALUES（值1，值2，…）；
- DELETE FROM 表名 [WHERE 条件表达式] 
- insert into 表名 (字段名1) select 字段名1 from 表名
## mysql的数据类型

## mysql创建表
- 根据时间戳更新是update的时候会自动更新,插入的时候不会更新
## insert的基本用法
- key重复的情况
```
on duplicate key update 
  domain = values(domain),
```
## mysql bug
- Column count doesn't match value count at row 1 插入的字段和实际的值个数不匹配
## mysql 函数
- 获取月份 month
- concat
