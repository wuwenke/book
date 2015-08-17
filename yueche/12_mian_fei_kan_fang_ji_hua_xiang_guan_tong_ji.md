#查询已有多少人次免费看房和多少楼盘已加入免费看房计划


* ** api : [/api/didi/getPersonHouseCount](/api/didi/getPersonHouseCount)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| callback | sring | no | jsonp 回调函数名称 |

* **return : json/jsonp**

```
{
    // 调⽤成功返回true，失败返回false
    "status" : true/fase,
    //状态码
    code:<int>,

    "msg" : "成功或失败的 描述",
    "data" : {
        "person_num" : "已成功预约的人次",
        "app_num": "已加入免费看房计划的楼盘数量"，
        "total_money" : "已有发放多少钱的打车券"
    }
}

```


* **requirement : 报名入口系统**
* **provider : 码上专车系统**
