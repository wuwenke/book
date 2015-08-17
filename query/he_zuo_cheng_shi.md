
# 获取合作楼盘城市列表

* ** api : [api/dataquery/getAllAppCityList ](api/dataquery/getAllAppCityList )** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| cityhid  | string | yes | 用户预约的专车目标楼盘编号，格式为 city_en + hid ，此楼盘 编号与 location_end 对应的地址是对应关系，即用户提交报名的楼盘页面对应的 楼盘编号 |
|mobile|int|no|预约用户的手机号 |
|date_time|int|no|格式为时间戳 , 注意此处为，看房日期, 默认为查询明天|
| callback | sring | no | jsonp 回调函数名称 |

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
  '3' => '参数不正确',
  '1000' => '请输入姓名',
  '1001' => '缺少city_en 和 hid',

  '1006' => '该楼盘不是滴滴合作项目',
  '1007' => '该楼盘没有参与活动或活动已过期或没有绑定规则',
  '1008' => '活动未审核',
  '1009' => '活动已过期',
  '1010' => '未设置活动规则',
  '1011' => '这一天不可以约车',
  '1012' => '未设置城市下单人约车次数限制',

  '1015' => '日期格式不正确',
  '1016' => '该用户已被添加在黑名单之列',

```


* **requirement : 报名入口系统/跟单系统**
* **provider : 码上专车系统**
