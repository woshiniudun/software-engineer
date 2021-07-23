- [swagger](https://swagger.io/docs/)
- [openAPI规范](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.0.2.md)
## bug
- [@Api不生效](https://blog.csdn.net/qq_38366063/article/details/89971234) 
## 基本用法 
- 访问swagger地址 base-url/swagger-ui.html
- [各种注解](https://blog.csdn.net/xiaojin21cen/article/details/78654652)
- @ApiOperation(value = "方法注释")
- @ApiModel("") 注释在POJO类上面
- 依赖,如果有冲突要改变版本
```
<dependency>
    <groupId>io.springfox</groupId>
    <artifactId>springfox-swagger2</artifactId>
    <version>2.2.2</version>
</dependency>
<dependency>
    <groupId>io.springfox</groupId>
    <artifactId>springfox-swagger-ui</artifactId>
    <version>2.2.2</version>
</dependency>
```
