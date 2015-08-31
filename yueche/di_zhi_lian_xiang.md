
# 地址联想

* ** api : [ /yueche/didi/add_complete]( /yueche/didi/add_complete)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|city|string|yes| 城市中文名|
|input |string|yes| 输入关键词|


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
        input: s,
        place_data: [
            {
            displayname: 首都机场,
            address: ,
            city: 北京市,
            area: 1,
            lng: 116.59686597618,
            lat: 40.082321212787
            },
            {
            displayname: 首都机场三号航站楼,
            address: ,
            city: 北京市,
            area: 1,
            lng: 116.61563086098,
            lat: 40.054939541696,
            },
            ...
        }
  }
```
* **返回错误码参照滴滴接口文档**




* **requirement : 码上专车系统**
* **provider : 码上专车系统**
