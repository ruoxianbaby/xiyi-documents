### **Service_api**

<a href="./#Service_api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>

### 测试主机host: 47.103.61.179:1022/  
- [user模块](./#user模块)  
    - [获取短信验证码](./#获取短信验证码)  
    - [获取access_token](./#获取access_token)
    - [获取用户信息接口](./#获取用户信息)  
    - [获取用户申请记录](./#获取用户申请记录)
    - [获取banner图片](./#获取banner图片)
    - [获取首页文章列表](./#获取首页文章列表)
    - [上传用户头像](./#上传用户头像)

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
- 请求参数:  

```json
{
    "mobile": 15821827706
}
```  
- 响应内容:  

```json
{
    "code": 1,
    "message": "获取成功",
    "info": {
        "sms_code": 5934
    }
}
```

### 获取access_token
- 请求方式: `post`
- 请求地址: {host}`get-access-token`
- 请求参数:  

```json
{
    "mobile": 15821827706, 
    "sms_code": 5934
}
```  
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "access_token": "uFYrhY7NUj68X9K_EbAFJ6axpWJVY70E"
    }
}
```

### 获取用户信息
- 请求方式: `get`
- 请求地址: {host}`users/0`


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 42,
        "mobile": "18308461696",
        "access_token": "4W1ZD1h_94Jmrx5PKqA24M-iuYvG8ce8",
        "nick_name": null,
        "avatar_image": null,
        "register_time": "2019-05-29 14:49:53",
        "last_login_time": "2019-05-29 14:49:53",
        "register_ip": 2147483647,
        "last_login_ip": 2147483647,
        "status": 1,
        "active": null,
        "active_time": null,
        "channel": null
    }
}
```  


### 获取banner图片
- 请求方式: `get`
- 请求地址: {host}`general/get-banner`


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "url": [
            "http://my_xijin_api.com/image/banner/1.jpg",
            "http://my_xijin_api.com/image/banner/2.jpg",
            "http://my_xijin_api.com/image/banner/3.jpg"
        ]
    }
}
```  



### 获取首页文章列表
- 请求方式: `get`
- 请求地址: {host}`articles`
- 请求参数:  per-page=10&page=2



- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 48,
                "type": null,
                "origin": "",
                "author": null,
                "title": "前44",
                "desc": null,
                "profile": null,
                "content": "&lt;p&gt;日期二无若群无&lt;/p&gt;",
                "create_time": "2019-07-22 11:23:49",
                "update_time": "2019-07-23 19:10:00",
                "creater": 108,
                "status": 0,
                "user_name": "nick108",
                "before_time": "3天前",
                "like_num": "0",
                "comment_num": "0",
                "img_url": ""
            },
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/articles?page=1"
            },
            "next": {
                "href": "http://my_xijin_api.com/articles?page=2"
            },
            "last": {
                "href": "http://my_xijin_api.com/articles?page=5"
            }
        },
        "_meta": {
            "totalCount": 92,
            "pageCount": 5,
            "currentPage": 1,
            "perPage": 20
        }
    }
}

---
before_time 多久之前
like_num 多少个喜欢
comment_num 评论数
img_url 图片的链接 没有就是空串
title 标题
desc 描述
user_name 昵称
avatar_image 用户头像
```  


### 上传用户头像
- 请求方式: `post`
- 请求地址: {host}`user/upload-avatar`
- 请求参数: 
```json
{
    "id": 110, 
    "image": "base64xxxxxxxxxxxx"
}
```  


- 响应内容:  

```json  
{
    "code": 1,
    "message": "上传成功",
    "info": "http://my_xijin_api.com./images/avatar_image/110.jpg"
}

---
id 上传头像的用户id
image base64格式的流
```  
