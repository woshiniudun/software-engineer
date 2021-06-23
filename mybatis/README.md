- [分页插件PageHelper](https://pagehelper.github.io/docs/)
- [mybatis文档](https://mybatis.org/mybatis-3/zh/index.html)
- [pageHelper.md](pageHelper.md)
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
## mybatis原理
