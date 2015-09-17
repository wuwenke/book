
# 获取正在参与活动的楼盘详情

* ** api : [/api/dataquery/getStartAppListByCity](/api/dataquery/getStartAppListByCity)** 

* **method : GET**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| city_en  | string | no | 城市英文 , 空时查询全国|
| key_word  | string | no | 楼盘名称 模糊匹配|
|pricerange|int|no|价格区间|
|housetype|int|no|户型|
|act_type|int|no|合作类型(默认是全部) 0是合作 1是非合作|
|limit|int|no|每页显示多少条数据 （可选参数 , 不填则所有） |
|page|int|no|页码 从1 开始  （可选参数 和 limit 一同使用）|


* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : null /暂无数据 
    "data" : {
          "hid": "楼盘ID",
          "name": "楼盘名称",
          "city_en": "楼盘英文",
          "actvity_id" : "活动ID",
          "activity_type" : "活动类型",  //0城市维度 1项目维度
          "act_type":"活动所属", // 0 开发商活动（合作）, 1乐居活动（非合作）
          "money" : <float>,   //单人单次约车金额， 如果改楼盘没有参与活动，那么此处是0，
          "longitude" : <float>, //地理位置，经度
          "latitude" : <float>, //地理位置，维度
          "address" : <string>, //楼盘所在地址
          "pic_s30" : <string>, //楼盘库图片
          "url" : <string>, //楼盘链接
          "district" : <string>, //楼盘区域
          "hometag" : <string>, //楼盘性质
          "price_display" : <string>, //楼盘的显示价格
          "housetype" : <int>, //楼盘户型 （接口参考1 返回值的value）
          "pricerange" : <int>, //楼盘的价格区间（接口参考2 返回值的value）
          ...
    }
}
```
* **返回错误代码 code 列举**

```
 暂无

```

* **接口参考：**

```
以下接口由楼盘库提供

1.城市下楼盘户型列表：http://data.house.sina.com.cn/api/get_dict.php?city=sc&type=common&district_flag=1&fields=housetype

2.城市下楼盘价格区间：http://data.house.sina.com.cn/api/get_dict.php?city=sc&type=common&district_flag=1&fields=pricerange
```

* **requirement : **
* **provider : 码上专车系统**
