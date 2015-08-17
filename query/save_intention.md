
# 获取正在参与活动的楼盘详情

* ** api : [/api/dataquery/insertUserintent](/api/dataquery/insertUserintent)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| city_en  | string | yes| 城市英文 |
|name|string|yes|用户姓名|
|mobile|int|yes|手机号|
|app_name|string|yes|意向楼盘名称|

* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : null /暂无数据 
    "data" : {
          "hid": "楼盘ID",
          "name": "楼盘名称",
          "city_en": "楼盘英文",
          “actvity_id” : “活动ID”,
          “activity_type” : “活动类型”,  //0城市维度 1项目维度
          “money” : <float>,   //单人单次约车金额， 如果改楼盘没有参与活动，那么此处是0
    }
}
```
* **返回错误代码 code 列举**

```
 暂无

```


* **requirement : **
* **provider : 码上专车系统**
