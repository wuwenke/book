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
|per_page|int|no|页码 从1 开始  （可选参数 和 limit 一同使用）|


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


* **requirement : **
* **provider : 码上专车系统**
