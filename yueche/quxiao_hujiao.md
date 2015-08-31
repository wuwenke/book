
# 取消叫车

* ** api : [ /yueche/didi/cancel_call]( /yueche/didi/cancel_call)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|real_order_id|string|yes| 实际订单id|
|force |int|no| 传入1时，强制取消；不传则默认为0，不强制取消|


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
        cost:20
        /*（非必返回字段）扣费金额，如果不传force且此订单已被司机抢单，就会返回cost字段（此订单未被取消，有可能产生扣费，需要确认），这时如果要强制取消订单,需要再次请求此接口且传force=1,这时此订单会发生扣款（此订单强制取消）*/
    }
  }
```
* **返回错误码参照滴滴接口文档**




* **requirement : 码上专车系统**
* **provider : 码上专车系统**
