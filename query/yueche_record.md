# 获取约车记录

* ** api : [/api/dataquery/getOrderInfoByMobile](/api/dataquery/getOrderInfoByMobile)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| mobile  | string | yes | 城市英文 , 空时查询全国|
| limit  | string | no | 楼盘名称 模糊匹配|
|limit|int|no|每页显示多少条数据 （可选参数 , 不填则所有） |
|per_page|int|no|页码 从1 开始  （可选参数 和 limit 一同使用）|


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