## 像思考JSONObject一样思考

和JSONObject处理思路类似的地方不着重阐述
## 类定义

```
public class JSONArray extends JSON implements List<Object>, Cloneable, RandomAccess, Serializable 
```

###    List<Object>
    数组通过List来标识
###    Cloneable、Serializable
    参考JSONObject相关分析
###   RandomAccess
    
    提升List性能使用，见“架构师的java基础\07 集合"中介绍
    此处去掉相关测试用例全部测试通过
    
    
    
##  关键成员

### 成员变量
transient关键字
java的transient关键字为我们提供了便利，你只需要实现Serilizable接口，将不需要序列化的属性前添加关键字transient，序列化对象的时候，这个属性就不会序列化到指定的目的地中。

如下代码中，因为用了关键字transient，真正需要序列化的就List<Object> list（这个和JSONObject中的Map<String, Object> map类似）
```
    private final List<Object> list;
    protected transient Object relatedArray;
    protected transient Type   componentType;
```

### 成员方法
和JSONObject类似，大多数方法是为了适配
implements List<Object>




### 