
# 获取看房打车券的面值金额和城市下打车券的份数

* ** api : [/api/dataquery/getCouponsInfo](/api/dataquery/getCouponsInfo)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| city_en  | string | yes| 城市英文 |

* **return : json**

```
{
    "status" : true/false
    “code”:<code>
    "msg" : null /已存在/保存成功/手机号格式不正确 
    "data" : null
}
```
* **返回错误代码 code 列举**

```
 暂无

```


* **requirement : **
* **provider : 码上专车系统**
