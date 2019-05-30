# 用户端api

- [user模块](./Api.md#user模块)  
    - [获取短信验证码](./Api.md#获取短信验证码)  
    - [获取access_token](./Api.md#获取短信验证码)
    - [获取用户信息接口](./Api.md#获取短信验证码)
- [产品模块]()


### 测试主机host: 47.103.61.179:81/  

### 全局header  

key |  vaule
----- | --------
Accept | application/json
Content-Type | application/json

需要验证的接口加上:  
key |  vaule
----- | --------
Authorization | Bearer ***access_token***


## user模块

### 获取短信验证码
- 请求方式: `post`
- 请求地址: {host}`get-sms-code`
- 请求参数: `{
    "mobile": 15821827706
}`
- 
