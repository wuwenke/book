
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
    // 扩展信息，如果当指定楼盘未参加滴滴专⻋业务或status返回false时， data可忽
    略
    data: {
        
    }
}
```
* **返回错误代码 code 列举**

```
暂无

```


* **requirement : 报名入口系统/跟单系统**
* **provider : 码上专车系统**
