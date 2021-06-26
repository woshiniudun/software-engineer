## maven依赖
注意第二项依赖于spring-boot-autoconfigure,可能会与本来引入的autoconfigure冲突
```
<!-- mybatis pager -->
<dependency>
    <groupId>com.github.pagehelper</groupId>
    <artifactId>pagehelper</artifactId>
    <version>5.1.10</version>
</dependency>
		<dependency>
			<groupId>com.github.pagehelper</groupId>
			<artifactId>pagehelper-spring-boot-autoconfigure</artifactId>
			<version>1.2.11</version>
			<exclusions>
				<exclusion>
					<groupId>org.springframework.boot</groupId>
					<artifactId>spring-boot-autoconfigure</artifactId>
				</exclusion>
			</exclusions>
		</dependency>
```
### 属性设置
```
pagehelper.helper-dialect=mysql
```
### 代码
```
PageHelper.startPage(pageNum, pageSize);
List<BcmBpartParentItemBO> data = mapper.listBpartParItemStatuses(query);
PageInfo<BcmBpartParentItemBO> pageInfo = new PageInfo<>(data);
Integer totalSize = pageInfo.getTotal();
```
## 排序
 8h12min![image](https://user-images.githubusercontent.com/51777429/123505991-7d435280-d694-11eb-8680-6f993e19c5cd.png)

