#取消实时呼叫车辆

* ** api : [/yueche/didi/cancel_call](/yueche/didi/cancel_call)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| real_order_id  | string | yes | 约车系统的实际|


* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : 正在呼叫中/呼叫失败
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
