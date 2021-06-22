- [stream用法大全](https://www.cnblogs.com/owenma/p/12207330.html)
## stream基本用法
- 取出对象的某个属性 List orderNoList=list.stream().map(Order::getOrderNo).collect(Collectors.toList());
- 将listgroupBy变成map 
```
Map<String, List<CommitCountResultBO>> maps = commitCountResultBOs.stream()
                .collect(Collectors.groupingBy(CommitCountResultBO::getDomain));
```
