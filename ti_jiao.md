
# 入口系统报名提交

* ** api : [/api/didi/smsverify](/api/didi/smsverify)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|mobile|int|yes| 用户表单填写的手机号 (仅针对国内运营商手机号) |
|name |string|yes/no|用户姓名(验证验证码有效性的时候 必须带入)|
|code |string|yes/no| 验证码（申请验证码操作 留空）|
|cityhid|string|yes/no|楼盘的city_en+hid 如 bj123 (验证验证码有效性的时候 必须带入)|
|source |string|yes|订单一级来源，平台标识|
|yx_act |string|no|营销活动标识|
|house_location|string|yes/no|楼盘地址 (验证验证码有效性的时候 必须带入)|
| callback | sring | no | jsonp 回调函数名称 |

* **return : json/jsonp**

```
{
    // 调⽤成功返回true，失败返回false
    status: true/false,

    //错误码
    code:xxxx,
    // 状态描述
    msg: '成功或失败的状态描述，⽂字信息',
    // 扩展信息，如果当指定楼盘未参加滴滴专⻋业务或status返回false时， data可忽
    略
    data: {

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

  '1015' => '日期格式不正确',
  '1016' => '该用户已被添加在黑名单之列',
  '1017' => '资金余额已不足',

```


* **requirement : 报名入口系统/跟单系统**
* **provider : 码上专车系统**
