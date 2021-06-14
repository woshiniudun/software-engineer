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
