- [官方网站]()
- [手册](http://logback.qos.ch/manual/architecture.html)
## 基本用法
- [在xml文件里面配置](https://blog.csdn.net/zbajie001/article/details/79596109)
- logback.xml和logback-test.xml是默认的配置文件，BasicConfigurator是默认配置 
```
<configuration scan="true" scanPeriod="60 seconds" debug="false"> 
  <contextName>myAppName</contextName> 
  <timestamp key="bySecond" datePattern="yyyyMMdd'T'HHmmss"/>  转换字符串格式
  <property name="APP_Name" value="myAppName" /> 
  <appender name="STDOUT" class="ch.qos.logback.core.ConsoleAppender"> 
    <encoder> 
      <pattern>%-4relative [%thread] %-5level %logger{35} - %msg %n</pattern> 
    </encoder> 
    <file>testFile.log</file> 
    <append>true</append> 
  </appender> 
  <root level="DEBUG"> 
    <appender-ref ref="STDOUT" /> 
  </root> 
 </configuration>
```
- 依赖
```
<dependency>
    <groupId>ch.qos.logback</groupId>
    <artifactId>logback-classic</artifactId>
</dependency>
```
- 日志级别 logging.level.root = DEGUG
## 手册
- appender、 layout 、logger是三个主要的类
- 
