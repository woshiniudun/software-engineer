## 文档
- [github wiki地址](https://github.com/alibaba/fastjson/wiki)
- [Getting Started](https://github.com/alibaba/fastjson/wiki/Samples-DataBind)
## 类转化
- 字符串 -> 列表
```java
List<Error>  errors = JSONObject.parseArray(jsonString, Error.class);
```
- JSONArray -> 列表
```
List<CommitcountBO> commitcountBOs = reusltJsonArray.toJavaList(CommitcountBO.class);
```
- 列表 -> JsonArray 
```
JSONArray array= JSONArray.parseArray(JSON.toJSONString(list))；
```
