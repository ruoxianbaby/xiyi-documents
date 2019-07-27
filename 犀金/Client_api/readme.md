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
    - [文章详情](./#文章详情)
    - [文章详情中的评论接口](./#文章评论)
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
- 请求地址: {host}`articles?fields=title,desc,avatar_image,admin_name,like_num,comment_num,img_url&per-page=2&page=2`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "title": "创业就像谈恋爱",
                "desc": null,
                "admin_name": "",
                "avatar_image": "",
                "like_num": "0",
                "comment_num": "0",
                "img_url": "https://xqimg.imedao.com/169b2bfdbe46c4393fdaa724.jpg"
            }
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
admin_name 后台管理员名
avatar_image 用户头像
preview_content 文章内容预览
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


###  文章详情
- 请求方式: `get`
- 请求地址: {host}`articles/:id`
- 请求参数: 


- 响应内容:  
title 标题  
content 文章内容  
article_like_num  文章喜欢总数  
like  自己是否点了喜欢按钮，0代表没有点，1是点了  
comment_num  评论总数  
collected 是否收藏，0代表没有收藏，1是收藏了  


```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "title": "葡萄酒专业到底在学啥？",
                "content": "<p class=\"ql-align-center\">一转眼又到了高考填志愿的季节。</p><p class=\"ql-align-center\"><br></p><p class=\"ql-align-center\">无数学子翻烂了志愿填报指南、参考学长学姐意见，各种途径打探，都想报一门好专业。</p><p class=\"ql-align-center\"><br></p><p class=\"ql-align-center\">近些年，一门专业在填报指南上的曝光率越来越高，它就是——</p><p class=\"ql-align-center\"><br></p><p class=\"ql-align-center\">葡萄酒专业</p>",
                "create_time": "2019-07-22 14:45:10",
                "like_num": "2",
                "like": 0,
                "comment_num": "3",
                "collect_num": "0",
                "collect": 0
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/articles?id=18&fields=title%2Ccreate_time%2Clike_num%2Clike%2Ccomment_num%2Ccollect_num%2Ccollect%2Ccontent&page=1"
            }
        },
        "_meta": {
            "totalCount": 1,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}

```  


###  文章评论
- 请求方式: `get`
- 请求地址: {host}`articles?id=18&fields=title,create_time,like_num,like,comment_num,collect_num,collect,content`
- 请求参数:   ?id 是文章的id


- 响应内容:  
content 评论内容  
nick_name  用户的昵称  


```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "content": "评论2",
                "create_time": "2019-07-25 15:23:13",
                "user_id": 108,
                "nick_name": "nick108"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/comments?article_id=18&per-page=1&page=2"
            },
            "first": {
                "href": "http://my_xijin_api.com/comments?article_id=18&per-page=1&page=1"
            },
            "prev": {
                "href": "http://my_xijin_api.com/comments?article_id=18&per-page=1&page=1"
            },
            "next": {
                "href": "http://my_xijin_api.com/comments?article_id=18&per-page=1&page=3"
            },
            "last": {
                "href": "http://my_xijin_api.com/comments?article_id=18&per-page=1&page=3"
            }
        },
        "_meta": {
            "totalCount": 3,
            "pageCount": 3,
            "currentPage": 2,
            "perPage": 1
        }
    }
}

```  
