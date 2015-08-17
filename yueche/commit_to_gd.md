
# 业务系统向跟单系统推送用户报名数据


* **描述**
```
测试地址 10.207.0.175  gendan.99.bch.leju.com
正式地址 kefu.leju.com
```

* ** api : [/?mod=api_didi&act=receive_record_info](/?mod=api_didi&act=receive_record_info)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|mobile|int|yes| 手机号 (仅针对国内运营商手机号) |
|name |string|yes|用户姓名|
|code |string|yes| 验证码|
|time|int|yes|用户专车预约时间，时间戳，指用户希望使用专车的时间|
|cityhid|string|yes|楼盘的city_en+hid 如 bj123 (验证验证码有效性的时候 必须带入)|
|source |string|yes|订单一级来源，平台标识 01 pc, 02 pad,03 weixin,04 chuping|
|yx_act |string|no|营销活动标识|
|location_start|string|yes|预约起始地址说明(文字)|
|location_end|string|yes|预约结束地址说明(文字)，在入口页面中， 通过业务楼盘获取 (非用户输入)|
| callback | sring | no | jsonp 回调函数名称 |

* **return : json/jsonp**

```
 {
    // 调⽤成功返回true，失败返回false
    status: true/false,
    //
    code:<int>,
    // 状态描述
    msg: '成功或失败的状态描述，⽂字信息',
    // 扩展信息
    data: {
      //第n位成功预约,
      serial_number：<int>

      //T+1 到 T+7 期间内是否已约满,只有当返回错误码是1020时返回
      week_full:<int>  1: 已满 ，0未满
    }
  }
```
* **返回错误代码 code 列举**

```
  '3' => '参数不正确',
  '1000' => '请输入姓名',
  '1001' => '缺少city_en 和 hid',

  '1003' => '城市名额超限',
  '1004' => '楼盘名额超限',
  '1005' => '验证失败',

  '1006' => '该楼盘不是滴滴合作项目',
  '1007' => '该楼盘没有参与活动或活动已过期或没有绑定规则',
  '1008' => '活动未审核',
  '1009' => '活动已过期',
  '1010' => '未设置活动规则',
  '1011' => '这一天不可以约车',
  '1012' => '未设置城市下单人约车次数限制',

  '1014' => '手机号不正确',
  '1015' => '日期格式不正确',
  '1016' => '该用户已被添加在黑名单之列',
  '1017' => '资金余额已不足',

  '1020' => '约车名额已满(预约看房当天)',

  '3001' => '本周总名额已约满',
  '3002' => '活动总名额已约满',

```


* **requirement : 报名入口系统**
* **provider : 码上专车系统**
