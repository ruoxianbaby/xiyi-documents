## **服务端api**
<a href="./#服务端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [Admin模块](./#用户模块)  
    - [获取access_token](./#获取access_token)  
    - [access_token换取用户信息](./#access_token换取用户信息)  

- [渠道模块](./#渠道模块)  
    - [当日数据](./#当日数据)  
    - [历史数据](./#历史数据)  
	
### 测试主机host: 47.103.61.179:8002/  

### 全局header  

key |  vaule
----- | --------
Accept | application/json
Content-Type | application/json

需要验证的接口加上:  
  
key |  vaule
----- | --------
Authorization | Bearer ***access_token***  

## 用户模块
### 获取access_token
- 请求方式: `post`
- 请求地址: {host}`/admin/get-access-token`
- 请求参数:  

```json
{
	"name": 15061690110,
	"password": "123456"
}
```  
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "access_token": "o2iSTUyXyr0ij-1m22KAuToup00JaZ1S"
    }
}
```
### access_token换取用户信息
- 请求方式: `get`
- 请求地址: {host}`/admin/info`
- 请求参数:  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 1,
        "name": "15061690110",
        "access_token": "o2iSTUyXyr0ij-1m22KAuToup00JaZ1S",
        "creater": null,
        "last_login_time": "2019-06-12 17:35:35",
        "last_login_ip": 2130706433,
        "register_time": null,
        "register_ip": null,
        "status": 1,
        "type": "1",
        "login_time": null
    }
}
```

## 渠道模块
### 当日数据
- 请求方式: `get`
- 请求地址: {host}`/channel/today-list`
- 请求参数:  

- 响应内容:  
reg -> 注册  
active -> 激活

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "channel_id": "13",
            "channel_name": "test",
            "channel_url": "http://wap.sshua.com/channel/1.html?channel_sign=1m-yljyfhU2Q7pusi1ZjhhBNRgy3MG-Q",
            "channel_qrcode": "images/qrcode/1m-yljyfhU2Q7pusi1ZjhhBNRgy3MG-Q.png",
            "uv": 2,
            "reg": 1,
            "active": 1
        }
    ]
}
```

### 历史数据
- 请求方式: `get`
- 请求地址: {host}`/channel/day-list`
- 请求参数:  

- 响应内容:  
reg -> 注册  
active -> 激活

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "channel_id": "13",
            "uv": 1,
            "reg": 1,
            "active": 0,
            "date": "2019-07-02",
            "channel_name": "test"
        },
        {
            "channel_id": "13",
            "uv": 1,
            "reg": 2,
            "active": 2,
            "date": "2019-07-01",
            "channel_name": "test"
        }
    ]
}
```
