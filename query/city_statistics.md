# 获取城市增量

* ** api : [/api/dataquery/getStatistics](/api/dataquery/getStatistics)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| start_time  | string | no | 时间区间的开始时间|
| end_time|string|no|时间区间的结束时间|
|limit|int|no|每页显示多少条数据 （可选参数 , 不填则所有） |
|page|int|no|页码 从1 开始  （可选参数 和 limit 一同使用）|


* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : null /无记录 
    "data" : 
        "cnt" :<int>,//数据总条数
        "list":[
        {
            "city_en"：<string>, //城市代码
            "commit_count" : <int>, //提交用户增量
            "succes_count" : <int>, //成功约车增量
          
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
