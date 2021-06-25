## API框架
- 
## 1.容器IOC
- @component让spring容器管理此类，相似功能的注解：@repository @service @controller
- ApplicationContext是beanFactory的升级版
-  @Autowired 四种模式，默认no，bytpe，byName，ref
- @Scope 默认单例，protoType，session，@Requestscope,等
- @SessionAtribute用于类上，可以会话内共享
- PropertyOverrideConfigurer 可以在properties设定属性、PropertySourcesPlaceholderConfigurer
- BeanFactoryPostProcessor是在spring容器加载了bean的定义文件之后，在bean实例化之前执行的
- 然后在调用初始化方法前后，执行了BeanPostProcessor
- [注解的基本原理](https://www.cnblogs.com/yangming1996/p/9295168.html)
  - 有些注解比如@override会被编译器作校验。 注解的本质就是一个继承了 Annotation 接口的接口
  - AnnotationInvocationHandler 
- [configuration](https://www.jianshu.com/p/721c76c1529c) 不过它是由AnnotationConfigApplicationContext类进行解析并注册到Bean的注册表中。
- @Profile("development")特定的profile下被激活
- @PropertySource，添加属性资源到Enviroment中
- @EnableLoadTimeWeaving @EnableAysnc @EnableSchedule等
- ApplicationContext除了beanFactory的附加功能：
  - ApplicationListener、ApplicationEvent 自动监听事件的触发，由ApplicationContext进行事件发布，事件实现notify方法，listener实现onApplicationEvent方法
  - MessageSource、ResourceLoader、ApplicationStartup
## 2.资源
- ServletContext
## 
