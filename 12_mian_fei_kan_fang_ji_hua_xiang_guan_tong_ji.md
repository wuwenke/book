#查询已有多少人次免费看房和多少楼盘已加入免费看房计划


* ** api : [/api/didi/getPersonHouseCount](/api/didi/getPersonHouseCount)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| callback | sring | no | jsonp 回调函数名称 |

* **return : json/jsonp**

```
{
    // 调⽤成功返回true，失败返回false
    "status" : true/fase,
    //状态码
    code:<int>,

    "msg" : "成功或失败的 描述",
    "data" : {
        "person_num" : "已成功预约的人次",
        "app_num": "已加入免费看房计划的楼盘数量"，
        "total_money" : "已有发放多少钱的打车券"
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
