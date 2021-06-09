## maven依赖
```
<dependency>
    <groupId>org.mybatis.spring.boot</groupId>
    <artifactId>mybatis-spring-boot-starter</artifactId>
    <version>1.5.10</version>
</dependency>
```
### 属性设置
```

```
### 代码
```
PageHelper.startPage(pageNum, pageSize);
List<BcmBpartParentItemBO> data = mapper.listBpartParItemStatuses(query);
PageInfo<BcmBpartParentItemBO> pageInfo = new PageInfo<>(data);
Integer totalSize = pageInfo.getTotal();
```
