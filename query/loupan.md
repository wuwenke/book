
# 获取正在参与活动的楼盘详情

* ** api : [/api/dataquery/getStartAppListByCity](/api/dataquery/getStartAppListByCity)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| cityhid  | string | yes | 用户预约的专车目标楼盘编号，格式为 city_en + hid ，此楼盘 编号与 location_end 对应的地址是对应关系，即用户提交报名的楼盘页面对应的 楼盘编号 |
|mobile|int|no|预约用户的手机号 |
|date_time|int|no|格式为时间戳 , 注意此处为，看房日期, 默认为查询明天|


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
