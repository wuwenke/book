
# 获取看房打车券的面值金额和全国的打车券的份数

* ** api : [/api/dataquery/insertUserintent](/api/dataquery/insertUserintent)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| city_en  | string | yes| 城市英文 |
|name|string|yes|用户姓名|
|mobile|int|yes|手机号|
|app_name|string|yes|意向楼盘名称|

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
