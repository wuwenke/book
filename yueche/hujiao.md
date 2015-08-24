#实时呼叫车辆

* ** api : [/yueche/didi/call](/yueche/didi/call)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| mobile  | string | yes | 乘客手机号|
| name  | string | yes | 乘客姓名|
|start_location|string|yes|出发地|
|s_lat|float|yes|出发地维度|
|s_lng|float|yes|出发地经度|
|end_location|string|yes|目的地|
|e_lat|float|yes|目的地维度|
|e_lat|float|yes|目的地经度|
|s_lat|float|yes|预约时间 时间戳|
|s_lat|float|yes|出发地维度|
|s_lat|float|yes|出发地维度|
|s_lat|float|yes|出发地维度|



* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : null /暂无数据 
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
