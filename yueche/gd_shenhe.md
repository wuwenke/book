
# 跟单系统向业务系统回推用户报名跟单数据


* ** api : [/api/didi/confirmed](/api/didi/confirmed)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|recordid |int|yes|订单编号
|mobile|int|yes| 手机号 (仅针对国内运营商手机号) |
|name |string|yes|用户姓名|
|time|int|yes|用户专车预约时间，时间戳，指用户希望使用专车的时间|
|cityhid|string|yes|楼盘的city_en+hid 如 bj123 (验证验证码有效性的时候 必须带入)|
|location_start|string|yes|预约起始地址说明(文字)|
|location_end|string|yes|预约结束地址说明(文字)，在入口页面中， 通过业务楼盘获取 (非用户输入)|
|price|float|yes|业务系统对报名用户起止地点设定的专车费用预算价格|
|operator_name|string|yes|业务系统审核人名称|
|operator_id|int|yes|业务系统审核人id|


* **return : json/jsonp**

```
  {
      // 调⽤成功返回true，失败返回false
      status: true/false,
      // 状态描述
      msg: '成功或失败的状态描述，⽂字信息'
  }
```
* **返回错误代码 code 列举**

```
无
```


* **requirement : 滴滴约车系统**
* **provider : 跟单系统**
