
# 重新叫车

* ** api : [ /yueche/didi/re_call]( /yueche/didi/re_call)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|real_order_id|string|yes| 实际订单id|


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
    data: {//
    }
  }
```
* **返回错误码参照滴滴接口文档**




* **requirement : 码上专车系统**
* **provider : 码上专车系统**
