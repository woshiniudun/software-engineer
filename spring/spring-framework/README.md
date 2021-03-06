- [reference](https://docs.spring.io/spring-framework/docs/current/reference/html/)
- [API](https://docs.spring.io/spring-framework/docs/current/javadoc-api/)
- [SpringMVC](./spring/spring-framework/spring-mvc)
- [spring-test](spring-test)
- [core](core)
- [aspectj编程指南](https://www.eclipse.org/aspectj/doc/released/progguide/index.html)
- [语言语义部分](https://www.eclipse.org/aspectj/doc/released/progguide/semantics-pointcuts.html)
## web 基本用法
- exceptionHandler
## aop基本用法
### spring + aspectJ
- execution @Aspect @Around @Pointcut(execution)  [blog](https://blog.csdn.net/yhl_jxy/article/details/78815636) 不要把@Aspect 放在@Service上面，会屏蔽代理
- 依赖
```
<dependency>      
    <groupId>org.springframework.boot</groupId>  
    <artifactId>spring-boot-starter-aop</artifactId>  
</dependency> 
```
- [aop的源码解析](https://blog.csdn.net/qq_26323323/article/details/81012855)
- 
- [aop的自调用问题](https://blog.csdn.net/z69183787/article/details/81252669)
- 如果要代理的目标对象至少实现了一个接口,使用java的动态代理
- [@configurable和@EnableSpringConfigured](https://www.jianshu.com/p/2f679ca07855) 没有用过
- [大致的原理](https://blog.csdn.net/xc123_java/article/details/90448446)
- [另一篇源码解析](https://blog.csdn.net/h294229025/article/details/100110636)
##  spring源码分析 
- [58篇](https://blog.csdn.net/qq_26000415/category_9271293.html)
- [@configuration注解的分析](https://blog.csdn.net/Koupoo/article/details/110304250)
- [30+篇](https://blog.csdn.net/qq_36882793/article/details/106745317)
- [aop源码解析](https://blog.csdn.net/qq_36882793/article/details/106745317)
- [getAdviceAndAdvisor](https://blog.csdn.net/qq_36882793/article/details/107070159)
- [targetSource](https://my.oschina.net/lixin91/blog/688188)
- [httpConverter原理]()
