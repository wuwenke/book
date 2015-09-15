
# 叫车

* ** api : [ /yueche/didi/call]( /yueche/didi/call)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|mobile|int|yes| 乘客手机号 (仅针对国内运营商手机号) |
|name |string|yes| 乘客姓名|
|departure_time|int|yes|用户预约乘车时间，时间戳，指用户希望用车的时间|
|cityhid|string|yes|楼盘的city_en+hid 如 bj123 (验证验证码有效性的时候 必须带入)|
|flat|float|yes|起始地纬度|
|flng|float|yes|起始地经度|
|start_name|string|yes|预约起始地名称(文字)|
|start_address|string|yes|预约起始地地址(文字)|
|end_name|string|yes|预约目的地详细地址(文字)|
| act_type | int | no | 活动类型：0城市维度活动 1项目维度活动|
| travel_type | int | no | 行程类型(默认取1)：1预约去程 2预约回程|
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
        order: {
            id: 4880109188406595918,
            city: 1,
            type: 0,
            call_phone: 13269661202,
            passenger_phone: 13269661202,
            status: 300,
            flng: 116.307479,
            flat: 40.045724,
            tlng: 116.800012,
            tlat: 39.689123,
            clng: 116.800012,
            clat: 39.689123,
            start_name: 得实大厦,
            start_address: 上地东路9号西南角,
            end_name: 万达广场,
            end_address: 北京市石景山区万达广场,
            departure_time: 2015-03-11 17:06:58,
            order_time: 2015-03-11 17:06:58,
            require_level: 100,
            extra_info: 这是订单备注,
        },
        combo: {
            time: 120,
            distance: 12.1,
            fee: 120.50
        },
        price: {
            estimate: 20.12
        }
    }
  }
```
* **返回错误代码 code 列举（除此之外的错误码参照滴滴接口文档）**

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


* **requirement : 码上专车系统**
* **provider : 码上专车系统**
