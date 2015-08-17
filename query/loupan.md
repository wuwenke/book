
# 获取正在参与活动的楼盘详情

* ** api : [/api/dataquery/getStartAppListByCity](/api/dataquery/getStartAppListByCity)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| city_en  | string | no | 城市英文 , 空时查询全国|
|limit|int|no|每页显示多少条数据 （可选参数 , 不填则所有） |
|page|int|no|页码 从1 开始  （可选参数 和 limit 一同使用）|


* **return : json**

```
{
    "status" : true
    “code”:null
    "msg" : null  
    "data" : {
           "city_en" : "城市英文名",
           "city " : "城市",
           "city_en" : "项目ID",
    }
}
```
* **返回错误代码 code 列举**

```
 暂无

```


* **requirement : **
* **provider : 码上专车系统**
