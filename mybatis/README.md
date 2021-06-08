- [分页插件PageHelper](https://pagehelper.github.io/docs/)
- [mybatis文档](https://mybatis.org/mybatis-3/zh/index.html)
## PageHelper用法
```Java
    PageHelper.startPage(curPage, pageSize);
    List<BcmBpartParentItemBO> data = mapper.listBpartParItemStatuses(query);
    PageInfo<BcmBpartParentItemBO> pageInfo = new PageInfo<>(data);
    result.setData(data);
    result.setTotalSize(pageInfo.getTotal());
```
## PageHelper原理
## mybatis用法
## mybatis原理
