
# 查询约车活动的时间规则

* ** api : [/api/didi/getActivityRule](/api/didi/getActivityRule)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| cityhid  | string | yes | 用户预约的专车目标楼盘编号，格式为 city_en + hid ，此楼盘 编号与 location_end 对应的地址是对应关系，即用户提交报名的楼盘页面对应的 楼盘编号 |
| callback | sring | no | jsonp 回调函数名称 |

* **return : json/jsonp**

```
{
    // 调⽤成功返回true，失败返回false
    status: true/false,

    //状态码
    code:<int>,

    // 状态描述
    msg: '成功或失败的状态描述，⽂字信息',

    // 扩展信息，如果当指定楼盘未参加滴滴专车业务或status返回false时， data可忽略
    data: {
        rule_type:<int>, //规则类型
        app_full ：<int> , 1楼盘名额已满，0楼盘有剩余
        longitude : <float>, //地理位置，经度
        latitude : <float>, //地理位置，维度
        address: <string>, //楼盘所在地址
        //约车时间范围和名额限制
        date_range":{
            "2015-06-13":{
                "limit":"6",    //名额限制
                "start":"14:00",    //开始时间
                "end":"15:00",      //结束时间
                "has_order":1,     //已约会员
                "remain_order":5   //剩余名额
                },
                ...
            }

    }
}

```
* **返回错误代码 code 列举**

```
  '3' => '参数不正确',
  '1001' => '缺少city_en 和 hid',

  '1006' => '该楼盘不是滴滴合作项目',
  '1007' => '该楼盘没有参与活动或活动已过期或没有绑定规则',
  '1008' => '活动未审核',
  '1009' => '活动已过期',
  '1010' => '未设置活动规则',
  '1011' => '这一天不可以约车',
  '1012' => '未设置城市下单人约车次数限制',

```


* **requirement : 报名入口系统/跟单系统**
* **provider : 码上专车系统**
