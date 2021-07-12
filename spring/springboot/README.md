## 特性
### 2. 外化配置
- application-{profile}
```
spring.application.name=MyApp
#---
spring.config.activate.on-cloud-platform=kubernetes 激活
spring.application.name=MyCloudApp 
```
- @ConfigurationProperties(prefix = "user1")可以 user1.name=Tom 与 类的属性匹配，
-   @DurationUnit  @DefaultValue @DataSizeUnit(DataUnit.MEGABYTES) /actuator/configprops
## acutator用法
- 依赖 <artifactId>spring-boot-starter-actuator</artifactId>
## application的所有属性
- [大全](https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html#application-properties)
## springboot的启动过程
- [启动过程](https://blog.wangqi.love/articles/Spring/SpringBoot%E5%90%AF%E5%8A%A8%E8%BF%87%E7%A8%8B.html)
- 
##  springboot源码分析 [58篇](https://blog.csdn.net/qq_26000415/category_9271293.html)
- [@configuration注解的分析](https://blog.csdn.net/Koupoo/article/details/110304250)
