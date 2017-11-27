 # JSONOjbect


invoke(Object proxy, Method method, Object[] args) throws Throwable {
InvocationHandler细致分析

public class JSONObject extends JSON 

implements Map<String, Object>
  为何要这么写

克隆方法什么时候被调用


# JSONArray
RandomAccess
    
    提升List性能使用，见“架构师的java基础\07 集合"中介绍
    

    protected transient Object relatedArray;
    protected transient Type   componentType;
    


# JSON
 等序列化完毕再完善
 