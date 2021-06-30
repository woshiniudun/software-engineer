- [junit5](https://junit.org/junit5/docs/current/user-guide/)
- [junit4](https://junit.org/junit4/)
## 基本用法
- 依赖
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-test</artifactId>
    <scope>test</scope>
</dependency>
```
- @SpringBootTest @RunWith(SpringRunner.class) 环境启动
- [assertions](https://github.com/junit-team/junit4/wiki/Assertions)
- [异常测试](https://github.com/junit-team/junit4/wiki/Exception-testing)
- 测试顺序，名字升序 @FixMethodOrder(MethodSorters.NAME_ASCENDING)
