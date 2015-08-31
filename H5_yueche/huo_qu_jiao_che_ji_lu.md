
# 获取叫车记录

* ** api : [ /yueche/didi/order_list]( /yueche/didi/order_list)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |



* **return : json/jsonp**

```
 {
    // 调⽤成功返回true，失败返回false
    status: true/false,
    //
    code:<int>,
    // 状态描述
    msg: '成功或失败的状态描述，⽂字信息',
    // 扩展信息
    data: {
            {
            order_id: 25,
            real_order_id: 1234565412458741235,
            member_name: sdfasdf,
            mobile: 15910611234,
            caller_mobile:15910611958,
            ...
            },
            {
            order_id: 451,
            real_order_id: 7895410578649875123,
            member_name: alex,
            mobile: 13710622234,
            caller_mobile:15910611958,
            ...
            },
             ...
        }
  }
```
* **返回错误码参照滴滴接口文档**




* **requirement : 码上专车系统**
* **provider : 码上专车系统**
