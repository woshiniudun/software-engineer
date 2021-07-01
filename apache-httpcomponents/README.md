- [文档](http://hc.apache.org/)   
- [github examples 异步的](https://github.com/apache/httpcomponents-client/blob/5.1.x/httpclient5/src/test/java/org/apache/hc/client5/http/examples/AsyncClientHttpExchange.java)
- [httpclient教程](http://hc.apache.org/httpcomponents-client-4.5.x/current/tutorial/html/index.html) 
## 基本用法
- 基本的get模板
```
CloseableHttpClient httpClient = RequestRestApiUtil.getHttpClient();
HttpGet httpget = new HttpGet(url);
httpget.setHeader("PRIVATE-TOKEN", userPrivateToken);
CloseableHttpResponse response= httpClient.execute(httpget);
HttpEntity entity = response.getEntity();
String jsonStr = EntityUtils.toString(entity, UTF8);
JSONArray groups = JSONArray.parseArray(jsonStr);
```
## bug
- [http请求跳过证书验证](https://blog.csdn.net/qq_38603819/article/details/87205463)
