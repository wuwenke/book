
# 获取楼盘以及会员相关配置信息

* ** api : [/api/didi/getconfig](/api/didi/getconfig)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| cityhid  | string | yes | 用户预约的专车目标楼盘编号，格式为 city_en + hid ，此楼盘 编号与 location_end 对应的地址是对应关系，即用户提交报名的楼盘页面对应的 楼盘编号 |
|mobile|int|no|预约用户的手机号 |
|date_time|int|no|格式为时间戳 , 注意此处为，看房日期, 默认为查询明天|
| type | int | no | 活动类型：0城市维度活动 1项目维度活动|
| callback | sring | no | jsonp 回调函数名称 |

* **return : json/jsonp**

```
{
    // 调⽤成功返回true，失败返回false
    status: true/false,
    // 状态描述
    msg: '成功或失败的状态描述，⽂字信息',
    // 当status为true时，返回具体数据
    data: {
        // 楼盘所在城市代码 `city_en`
        city: <string>,
        // 楼盘hid
        hid: <int>,
        //活动ID,
        activity_id:<int>,
        //楼盘所属城市下，单人报名总次数限制
        city_limit: <int>,
        // 楼盘名称
        name: <string>,
        // 楼盘所在地址信息
        location: <string>,
        longitude : <float>, //地理位置，经度
        latitude : <float>, //地理位置，维度
        // 在date_time这一天尚可预约报名的名额，如果周满或总名额也满，那么此处为0
        unfilled: <int>,
        // 项目 在date_time这一天 总共可预约报名的名额总共可预约报名的名额
        total: <int>,
        // 单⼈单次约车费⽤上限
        maxprice: <float>,
        // 单⼈预约次数限制
        limit: <int>,
        //预约日期剩余名额
        user_limit: <int>,
        app_banner: 'http://ssfda.com/sdf.jpg', //微信端使用的楼盘缩列图
        share_info: '', //微信分享文案,
        note : '', //活动通知信息
        note_url : '',//活动通知多对应的URL
        //在城市下剩余报名次数（带参数 手机号）,
        city_unfilled: <int>,
        //对某楼盘的剩余报名次数(带参数 手机号)
        app_unfilled: <int>,
        //项目余额
        balance:<float>,
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
