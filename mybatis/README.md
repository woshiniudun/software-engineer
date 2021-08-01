- [分页插件PageHelper](https://pagehelper.github.io/docs/)
- [mybatis文档](https://mybatis.org/mybatis-3/zh/index.html)
- [pageHelper.md](pageHelper.md)
## 常见bug
- 首先是字段的驼峰和下划线格式注意
- 其次是test里面的语言是java语言的形式
- uniq键里面有null
## PageHelper原理
## mybatis基本用法
- mybatis.configuration.map-underscore-to-camel-case=true 开启开关：表字段自动对应实体类里面的驼峰格式字段
```
配置类里设置，而且要放在资源加载配置的后面，很神奇。
@Bean(name="sqlSessionFactory")
    public SqlSessionFactory sqlSessionFactory(@Qualifier("dataSource") DataSource dataSource) throws Exception {
        SqlSessionFactoryBean sqlSessionFactoryBean = new SqlSessionFactoryBean();
        sqlSessionFactoryBean.setDataSource(dataSource);
        sqlSessionFactoryBean.getObject().getConfiguration().setMapUnderscoreToCamelCase(true);
        return sqlSessionFactoryBean.getObject();
    }
```
- [分支选择](https://www.cnblogs.com/xiximayou/p/12221581.html)
## mybatis原理
- sql标签是用来复用的语句
## mybatis异常
- Invalid bound statement
## 源码分析
- [Mybatis源码详细分析（最新最全）-csdn](https://blog.csdn.net/qq_34295193/article/details/111193065)
- [statement和configuration的源码分析](https://blog.csdn.net/ShewMi/article/details/80242339)
- [executor的源码分析](https://blog.csdn.net/ShewMi/article/details/80283094)
##
