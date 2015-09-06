# 获取城市增量

* ** api : [/api/dataquery/getStatistics](/api/dataquery/getStatistics)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| caller_mobile  | string | no | 在白名单列表里中的手机号，即订单代叫人的手机号|
| mobile|string|no|客户手机号|
|real_order_id|string|no|实际订单编号|
|limit|int|no|每页显示多少条数据 （可选参数 , 不填则所有） |
|page|int|no|页码 从1 开始  （可选参数 和 limit 一同使用）|


* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : null /暂无数据 
    "data" : [
        {
            "order_id"：<int>, //码上专车自己的订单编号
            "real_order_id" : <int>, //第三方打车系统的实际订单ID
            "mobile" : <int>, //乘客手机号
            "name" : <stirng> , //乘客姓名
            "real_status" : <code> ,//第三方打车系统的订单状态
            "appointment_time" ：<int> //预约时间戳
        }
    ]
}

```
* **返回错误代码 code 列举**

```
 暂无

```
* **订单状态**

|【滴滴】状态码|描述|
|--|--|
|300| 	等待应答|
|311 |	订单超时|
|400 |	等待接驾|
|410 |	司机已到达|
|500 |	行程中|
|600 |	行程结束|
|610 |	行程异常结束|
|700| 	已支付 |

* **requirement : **
* **provider : 码上专车系统**
