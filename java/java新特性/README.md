- [stream用法大全](https://www.cnblogs.com/owenma/p/12207330.html)
## stream基本用法
- 取出对象的某个属性 List orderNoList=list.stream().map(Order::getOrderNo).collect(Collectors.toList());
- 将listgroupBy变成map 
```
Map<String, List<CommitCountResultBO>> maps = commitCountResultBOs.stream()
                .collect(Collectors.groupingBy(CommitCountResultBO::getDomain));
```
- 加list groupBy 并且加总某个字段值
- collect：接收一个Collector实例，将流中元素收集成另外一个数据结构。
- map：接收一个函数作为参数，该函数会被应用到每个元素上，并将其映射成一个新的元素。

