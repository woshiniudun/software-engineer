## bug
- mysql的语法和java不一样，判断非空用！=null不行，得用is not null
## 增删改查基本用法 [博客](https://www.cnblogs.com/heyangblog/p/7624645.html)
- INSERT INTO 表名（字段名1，字段名2，…）VALUES（值1，值2，…）；
- DELETE FROM 表名 [WHERE 条件表达式] 
- insert into 表名 (字段名1) select 字段名1 from 表名
- truncate table xxx 清空表数据，[删除多张表和一张表](https://blog.csdn.net/weixin_41380972/article/details/86627193)
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
- invalid use of null [解决办法](https://blog.csdn.net/lxw1844912514/article/details/100028222)
## mysql 函数
- 获取月份 month
- [concat](https://www.cnblogs.com/aiyr/p/6830593.html)
- DATE_FORMAT(end_time, 'yyyy-MM-dd)取出日期字段的时候设置一下格式 [格式](https://blog.csdn.net/blinking_star/article/details/72771285)
- [获取当年的第一天、最后一天](https://www.cnblogs.com/1996swg/p/9254492.html)
## mysql 语法
- [大小写的替换](https://www.cnblogs.com/jpfss/p/10254923.html)
- [union和union all的区别](https://www.cnblogs.com/xiangshu/articles/2054447.html)
## 建表
```
CREATE TABLE IF NOT EXISTS `runoob_tbl`(
   `runoob_id` INT UNSIGNED AUTO_INCREMENT,
   `runoob_title` VARCHAR(100) NOT NULL,
   `runoob_author` VARCHAR(40) NOT NULL,
   `submission_date` DATE,
   PRIMARY KEY ( `runoob_id` )
)ENGINE=InnoDB DEFAULT CHARSET=utf8;
ALTER  table dwr_scm_pln_item_demand_f_t add unique index  unique_index (lv1_prod_rd_team_cn_name, hw_contract_num, item_code, prod_code, period_date) USING BTREE;
```
