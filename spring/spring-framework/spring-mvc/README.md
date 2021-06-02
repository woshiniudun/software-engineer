
- [wesocker rfc](https://datatracker.ietf.org/doc/html/rfc6455#section-1.7)
# 1.Spring Web MVC
springmvc基于servlet API并且部署到servlet容器</br>
[servlet菜鸟教程](https://www.runoob.com/servlet/servlet-useful-resources.html)
## 1.1 DispatcherServlet
### 1.1.1. 上下文层次结构
![image](https://user-images.githubusercontent.com/51777429/120431233-cd3b3c00-c3aa-11eb-8a4a-e14a2212e16d.png)
### 1.1.4. Servlet Config
用来配置filter、dispatcher、ApplicationContext等等</br>
可以尝试不用springboot跑起一个helloword</br>
### 1.1.5. Processing
绑定各种resolver
### 1.1.7. Interception
有prehandle、postHandle、afterCompletion等方法</br>
### 1.1.8. 例外
HandlerExceptionResolver 有几类具体可以到文档里看</br>
@ResponseStatus</br>
### 1.1.12. Multipart Resolver
[commoms fileupload](https://commons.apache.org/proper/commons-fileupload/)或者是用mutilpartsolver实现文件上传</br>

## 1.2. Filters
- ForwardedHeaderFilter
- FormContentFilter
- ShallowEtagHeaderFilter
- CorsFilter
## 1.3. Annotated Controllers
- @GetMapping
- @PathVariable
- @ExceptionHandler
- @ControllerAdvice
- @InitBinder
- PATH匹配的时候其实有个比较器用来path，比如通配符/** 优先级就比较低
- 后缀匹配现在弃用了,可以使用header中的accept字段来判断内容@RequestHeader(value="User-Agent")
- [RFD反射文件下载攻击技术](https://zhuanlan.zhihu.com/p/161166505)可以执行bat文件，通过设置下载文件类型为
- @GetMapping(path = "/pets", headers = "myHeader=myValue"，params="myParam=myValue",produces={},consume={}) 
### 1.3.3. Handler Methods
- @RequestPart
- @SessionAttribute
- @CookieValue
- HttpEntity<B>
- HttpEntity<B>, ResponseEntity<B>
- @Nullable
- @MatrixVariable
- @RequestHeader("Accept-Encoding") @RequestHeader("Keep-Alive") 自动类型转换
- @CookieValue("JSESSIONID") String cookie
- @ModelAttribute("pet") Pet pet, BindingResult result
- Pet pet, BindingResult errors, SessionStatus status
- @SessionAttribute User user @RequestAttribute Client client
- 重定向return "redirect:files/{path}"


