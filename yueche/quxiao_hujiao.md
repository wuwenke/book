#取消实时呼叫车辆

* ** api : [/yueche/didi/cancel_call](/yueche/didi/cancel_call)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| real_order_id  | string | yes | 约车系统的实际|
|force|string|no|强制取消订单,当订单处于带应答状态时，该参数不用传（‘true’ / 'false'）|


* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : 描述
    "data" : {

    }
}
```
* **返回错误代码 code 列举**

```
 暂无

```


* **requirement : **
* **provider : 码上专车系统**
