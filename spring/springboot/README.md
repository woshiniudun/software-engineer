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
- @profileActive@ 可以在target里面看到具体是啥 ，maven profile的来源我估计一个是.properties的后缀，2是
## springboot的启动过程
- [启动过程](https://blog.wangqi.love/articles/Spring/SpringBoot%E5%90%AF%E5%8A%A8%E8%BF%87%E7%A8%8B.html)
- [读取配置类](https://blog.csdn.net/Koupoo/article/details/110304250)
- @EnableAutoConfiguration可以帮助SpringBoot应用将所有符合条件的@Configuration配置都加载到当前SpringBoot创建并使用的IoC容器。
