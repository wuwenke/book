
# 发送验证码及登陆验证

* ** api : [/api/dataquery/login](/api/dataquery/login)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|mobile|int|yes| 手机号 |
|code |string|yes/no| 验证码（验证流程用到申请验证码操作 留空）|
|source |string|yes|订单一级来源，平台标识 01(pc), 02(pad),03(weixin),04chuping,05kdlj,06 后台,07,08移动平台


* **return : json**

```
{
    // 调⽤成功返回true，失败返回false
    status: true/false,

    //错误码
    code:xxxx,
    // 状态描述
    msg: '成功或失败的状态描述，⽂字信息',
    
    data: {
        
    }
}
```
* **返回错误代码 code 列举**

```
暂无

```


* **requirement : **
* **provider : 码上专车系统**
