
# 获取看房打车券的面值金额和全国下打车券的份数

* ** api : [/api/dataquery/getCouponsInfo](/api/dataquery/getCouponsInfo)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| city_en  | string | yes| 城市英文 |
|hid|string|no|楼盘HID|


* **return : json**

```
{
    "status" : true/false
    “code”:<code>
    "msg" : ‘接口描述信息’
    "data" : {
        “max_money”: <float> , 城市下 最高的单人单次约车金额
        “city_fraction” :<int> 全国活动总名额之和
        "city_week_fraction": <int> 查询城市在当前周的总名额之和
        "house_week_fraction": <int> 查询楼盘在当前周的总名额之和（不传hid，此处为0）
    }
}

说明： max_money 当城市下无参与活动的楼盘是  该值取全国的单人最高金额
```
* **返回错误代码 code 列举**

```
 暂无

```


* **requirement : **
* **provider : 码上专车系统**
