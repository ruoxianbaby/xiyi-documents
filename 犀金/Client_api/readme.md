### **Client_api**

<a href="./#client_api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>

### 测试主机host: 47.103.61.179:1022/  
- [user模块](./#user模块)  
    - [获取短信验证码](./#获取短信验证码)  
    - [获取access_token](./#获取access_token)
    - [获取用户信息接口](./#获取用户信息)   
    - 上传用户头像  
    	先调用[上传图片](./#上传图片接口)的接口,再调用[更新用户信息](./#更新用户信息)的接口
    - [更新用户信息](./#更新用户信息)  
    - [检查是否绑定](./#检查是否绑定微信qq)
    - 绑定微信qq  
    	参考[更新用户信息](./#更新用户信息)的接口
    - [主页浏览](./#主页浏览)
        - [新增主页浏览记录](./#新增主页浏览记录)
	- 查看今日,历史浏览人数  
		参考[获取用户信息接口](./#获取用户信息)接口
    - [我的收藏](./#我的收藏)
    - [历史记录](./#历史记录)
- [搜索](./#搜索)
    - [文章搜索](./#文章搜索)
    - [用户搜索](./#用户搜索)
- [通用模块](./#通用模块)
	- [用户反馈](./#用户反馈)
	- [上报设备号](./#上报设备号)  
	- [上传图片接口](./#上传图片接口)
	- [get贷超url](./#get贷超url)
- [app相关](./#app相关)
    - [app版本更新](./#app版本更新)
    - [app工作url](./#app工作url)
- [banner模块](./#banner模块)
    - [获取banner图片](./#获取banner图片)
- [文章模块](./#文章模块)
    - [获取首页文章列表](./#获取首页文章列表)
    - [文章详情](./#文章详情)
    - [文章详情中的评论接口 没有点进去的](./#文章评论)
    - [文章点赞收藏关注toggle](./#文章点赞收藏关注toggle)
    - [添加文章评论](./#添加文章评论)
    - [删除评论](./#删除评论)
    - [更多评论点进去的最新评论](./#更多评论点进去的最新评论)
    - [更多评论点进去的最热评论](./#更多评论点进去的最热评论)
    - [评论点赞toggle](./#评论点赞toggle)
    - [评论详情](./#评论详情)
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
    "info": ""
}
```

### 获取access_token
- 请求方式: `post`
- 请求地址: {host}`get-access-token`
- 请求参数:  

```json
{
    "mobile": 15821827706, 
    "sms_code": 5934,
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
- 请求地址: {host}`users/:id`
> 参数说明: 拼接上`?expand=today-browse,total-browse` 可查看今日和总浏览数
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
### 更新用户信息
- 请求方式: `put`
- 请求地址: {host}`user/update`
- 请求参数:
```json
{
	"nick_name": "dada",
	"wechat_token": "dad",
	"qq_token": "djehwgqwj"		
}
```
- 响应内容:  

```json  
{
    "code": 1,
    "message": "更新成功",
    "info": {
        "id": 1,
        "nick_name": "dada",
        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
        "register_time": "2019-07-11 14:33:50",
        "register_ip": "127.255.255.255"
    }
}
```  
### 检查是否绑定微信qq
- 请求方式: `get`
- 请求地址: {host}`user/check-bind?wechat_token=dad`
- 请求参数:  `wechat_token=dad` 或者 `qq_token=dahkn`  
- 响应内容:  
```json  
{
    "code": 1,
    "message": "已绑定",
    "info": {
        "id": 1,
        "nick_name": "dada",
        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
        "register_time": "2019-07-11 14:33:50",
        "wechat_token": "dad",
        "qq_token": "djehwgqwj",
        "register_ip": "127.255.255.255"
    }
}
``` 

### 主页浏览  
### 新增主页浏览记录  
- 请求方式: `post`
- 请求地址: {host}`user-profile-browses`
- 请求参数:  
```json
{
    "browse_user_id": 21
}
```  
- 响应内容:  
```json  
{
    "code": 1,
    "message": "",
    "info": ""
}
```  
### 我的收藏
- 请求方式: `get`
- 请求地址: {host}`article-collects?user_id=1`
- 请求参数: `user_id=1` 
- 响应内容:  
```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 19,
                "user_id": 1,
                "article_id": 61,
                "title": "创业就像谈恋爱",
                "preview_image": "http://img.wine-talk.cn/data/news/image/20190627/20190627150612_27223.jpg",
                "desc": "miaoshu",
                "comment_num": "0",
                "like_num": "0",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png"
            },
            {
                "id": 26,
                "user_id": 1,
                "article_id": 63,
                "title": "三大核心板块，轻松掌握电商运营",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-07-24/e4dde71190ef76c69bf19d0adbcf4bfeae5167c9.jpeg",
                "desc": "miaoshu",
                "comment_num": "0",
                "like_num": "0",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/article-collects?user_id=1&page=1"
            }
        },
        "_meta": {
            "totalCount": 2,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```
### 历史记录
- 请求方式: `get`
- 请求地址: {host}`users/my-browse-record?page=&per-page=`
- 响应内容:  
```json  
{
    "code": 1,
    "message": "",
    "info": {
        "items": [
            {
                "id": "63",
                "title": "三大核心板块，轻松掌握电商运营",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-07-24/e4dde71190ef76c69bf19d0adbcf4bfeae5167c9.jpeg",
                "desc": "miaoshu",
                "like_num": "0",
                "comment_num": "2",
                "my_view_count": "2"
            },
            {
                "id": "65",
                "title": "葡萄酒投资回报超股票黄金",
                "preview_image": "http://img.wine-talk.cn/data/news/image/20190627/20190627150612_27223.jpg",
                "desc": "miaoshu",
                "like_num": "0",
                "comment_num": "0",
                "my_view_count": "1"
            }
        ],
        "_meta": {
            "totalCount": "9",
            "pageCount": 5,
            "currentPage": "1",
            "perPage": "2"
        }
    }
}
```
### 搜索
### 用户搜索
- 请求方式: `get`
- 请求地址: {host}`users?nick_name=da`
> 参数 `nick_name=da` 模糊搜索
- 响应内容:  
```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "nick_name": "dad2",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                "register_time": "2019-07-11 14:33:50",
                "wechat_token": "dad",
                "qq_token": "djehwgqwj",
                "access_token": "o2iSTUyXyr0ij-1m22KAuToup00JaZ1S",
                "register_ip": "31.84.183.44"
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8001/users?nick_name=da&page=1"
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

### 文章搜索
- 请求方式: `get`
- 请求地址: {host}`articles?title=葡萄`
> 参数 `title=葡萄 模糊搜索
- 响应内容:  
```json  

```
### 通用模块
### 用户反馈  
- 请求方式: `post`
- 请求地址: {host}`generals/feedback`
- 请求参数:   
```json
{
    "type": 1,
    "user_id": 10,
    "feedback_type": 1,
    "content": "你的🐎死了"
}
```  

### 上报设备号  
- 请求方式: `post`
- 请求地址: {host}`submit-device`
- 请求参数:   
```json
{
  "user_id": 1,
  "device_token": "123456",
  "client_id": "da",
  "platform": 1
}
```  
- 参数说明: `device_token`设备号, `client_id`友盟唯一标识, `platform`1Android,2ios,2web,4wechat,5others

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": ""
}	
``` 
### 上传图片接口  
- 请求方式: `post`
- 请求地址: {host}`generals/upload-file-and-to-aliyun_oss?type=avatar`
- 请求参数 `type=avatar`, `type` 说明:支持 avatar, article 等等
```json
{
    "file": [binary]
}
```  
- 响应内容:
```json
{
    "code": 1,
    "message": "上传成功",
    "info": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-30/jVPW6-x-jkY0s8zoOAm7lGslg0q9ebbZ.jpg"
}
```

### 获取banner图片
- 请求方式: `get`
- 请求地址: {host}`general/get-banner`


- 响应内容:  
id -> 文章的id
```json  
{
    "code": 1,
    "message": "操作成功",
    "info": [
        {
            "id": "61",
            "image": "https://xqimg.imedao.com/169b2bfdbe46c4393fdaa724.jpg"
        },
        {
            "id": "62",
            "image": "https://xqimg.imedao.com/169b2bfdbe46c4393fdaa724.jpg"
        },
        {
            "id": "63",
            "image": "https://xqimg.imedao.com/169b2bfdbe46c4393fdaa724.jpg"
        }
    ]
}
```  

## app相关
### app版本更新
- 请求方式: `get`
- 请求地址: {host}`generals/app-check-version`
- 请求参数: 
```json
{
    "os": 1, // 系统1android,2ios,3web,4其他
    "channel": "百度" // 渠道名
}
```  

- 响应内容:  
```json  
{
    "code": 1,
    "message": "",
    "info": {
        "id": 2,
        "name": "test",
        "os": null,
        "channel": null,
        "status": 1,
        "auditing": null, //审核状态, 1 正在审核
        "version": null,
        "app_url": null,
        "force": null // 是否强制更新 1是
    }
}
```

### app工作url
- 请求方式: `get`
- 请求地址: {host}`app-settings/1?os=&version=&channel=`
- 请求参数: 

- 响应内容:  
```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 1,
        "webview_url": "https://xijin.sshua.com/index.html"
    }
}
```


### 获取首页文章列表
- 请求方式: `get`
- 请求地址: {host}`articles?sort=-id`
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
                "author": "",
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

###  文章详情
- 请求方式: `get`
- 请求地址: {host}`articles?id=183&expand=content,comment,label,recommend`
- 请求参数: 


- 响应内容:  
title 标题  
content 文章内容  
article_like_num  文章喜欢总数  
like  自己是否点了喜欢按钮，0代表没有点，1是点了  
comment_num  评论总数  
collected 是否收藏，0代表没有收藏，1是收藏了  
focus 1 代表已经关注了该作者  
origin 文章来源  
author  作者  
desc 副标题  
preview_image 文章的顶部图片  
recommand 文章推荐，至多返回3个，没有则为空
label 文章标签

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
		"focus": 1,
		"label": [
                    {
                        "id": "1",
                        "name": "标签1"
                    },
                    {
                        "id": "2",
                        "name": "标签2"
                    },
                    {
                        "id": "3",
                        "name": "标签3"
                    }
                ],
		"recommand": [
                    {
                        "id": "77",
                        "images": "http://img.wine-talk.cn/data/news/image/20190627/20190627150612_27223.jpg",
                        "title": "瓶颈是什么，我们是应该拥抱瓶颈还是逃避瓶颈？",
                        "like_num": "0",
                        "comment_num": "0"
                    },
                    {
                        "id": "78",
                        "images": "http://img.wine-talk.cn/data/news/image/20190627/20190627150612_27223.jpg",
                        "title": "5G时代，拿什么来拯救你的职场焦虑？",
                        "like_num": "0",
                        "comment_num": "0"
                    },
                    {
                        "id": "61",
                        "images": "http://img.wine-talk.cn/data/news/image/20190627/20190627150612_27223.jpg",
                        "title": "创业就像谈恋爱",
                        "like_num": "1",
                        "comment_num": "0"
                    }
                ]
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
- 请求地址: {host}`articles?id=18&expand=comment`
- 请求参数:   ?id 是文章的id


- 响应内容:  
like_num是多少个点赞
like 0 代表该用户未点赞，1代表点了赞

```json  
{
    "code": 1,
    "message": "success",
        "info": {
        "items": [
            {
                "comment": [
                    {
                        "id": "2",
                        "content": "评论2",
                        "create_time": "2019-07-25 15:23:13",
                        "user_name": "nick108",
			"like": "0",			
			"like_num": "2",
			"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/107.jpg",
                        "time_before": "1天前"
                    },
                    {
                        "id": "3",
                        "content": "评论3",
                        "create_time": "2019-07-25 15:23:16",
                        "user_name": "nicheng222",
			"like": "1",
			"like_num": "2",
			"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/107.jpg",
                        "time_before": "1天前"
                    },
                    {
                        "id": "5",
                        "content": "测试测试测试",
                        "create_time": "2019-07-27 14:21:39",
                        "user_name": "nick108",
			"like": "0",
			"like_num": "2",
			"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/107.jpg",
                        "time_before": "55分钟前"
                    }
                ],
            }
        ]
}

```  



###  文章点赞收藏关注toggle
- 请求方式: `put`
- 请求地址: {host}`articles/18?type=1`
- 请求参数:   18是文章id，type 1代表喜欢，2代表收藏，3代表关注


- 响应内容:  
- active  0 代表切换成了没点赞状态，1代表成了已点赞


```json  
{
    "code": 1,
    "message": "切换成功",
    "info": {
        "active": 0
    }
}

```  




###  删除评论
- 请求方式: `delete`
- 请求地址: {host}`comments/1`
- 请求参数:  
id 评论的id  

- 响应内容:  

```json  
{
    "code": 0,
    "message": "删除成功",
    "info": ""
}

```  

###  更多评论点进去的最新评论
- 请求方式: `get`
- 请求地址: {host}`comments?article_id=58&pid=0&per-page=2&page=1&sort=-id`
- 请求参数:  
article_id 文章的id  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "article_id": 58,
                "user_id": 1,
                "content": "aaa",
                "pid": 0,
                "reply_pid": 0,
                "like": 0,
                "child_count": 2,
                "create_time": "2019-07-31 14:29:03",
                "update_time": null,
                "del": null,
                "comment_count": "4",
                "nick_name": "dad2",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                "like_count": "0",
                "child": [
                    {
                        "id": "2",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "aaa",
                        "pid": "1",
                        "reply_pid": "1",
                        "like": 0,
                        "child_count": "0",
                        "create_time": "2019-07-31 14:29:14",
                        "update_time": null,
                        "del": null,
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like_count": "4",
                        "child_reply": 0
                    },
                    {
                        "id": "3",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "ccccaaa",
                        "pid": "1",
                        "reply_pid": "2",
                        "like": 0,
                        "child_count": "0",
                        "create_time": "2019-07-31 14:29:21",
                        "update_time": null,
                        "del": null,
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like_count": "1",
                        "child_reply": 1,
                        "replied_user_id": 1,
                        "replied_nick_name": "dad2"
                    }
                ]
            },
            {
                "id": 4,
                "article_id": 58,
                "user_id": 1,
                "content": "xxxx",
                "pid": 0,
                "reply_pid": 0,
                "like": 0,
                "child_count": 0,
                "create_time": "2019-07-31 14:30:26",
                "update_time": null,
                "del": null,
                "comment_count": "4",
                "nick_name": "dad2",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                "like_count": "0",
                "child": []
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/comments?article_id=58&pid=0&per-page=2&page=1&sort=-child_count"
            }
        },
        "_meta": {
            "totalCount": 2,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 2
        }
    }
}
child_reply  是否有评论，1代表有
replied_user_id  被评论的人的id
replied_nick_name 被评论人的昵称
id 是当前评论的id
comment_count 是这篇文章的评论总数
like 是当前用户是否对这个评论点赞 1代表是
like_count 是这条评论已经被点了多少次的赞
child 是这条评论下的子评论
```  

###  更多评论点进去的最热评论
- 请求方式: `get`
- 请求地址: {host}`comments?article_id=58&pid=0&per-page=2&page=1&sort=-child_count`
- 请求参数:  
article_id 文章的id  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "article_id": 58,
                "user_id": 1,
                "content": "aaa",
                "pid": 0,
                "reply_pid": 0,
                "like": 0,
                "child_count": 2,
                "create_time": "2019-07-31 14:29:03",
                "update_time": null,
                "del": null,
                "comment_count": "4",
                "nick_name": "dad2",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                "like_count": "0",
                "child": [
                    {
                        "id": "2",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "aaa",
                        "pid": "1",
                        "reply_pid": "1",
                        "like": 0,
                        "child_count": "0",
                        "create_time": "2019-07-31 14:29:14",
                        "update_time": null,
                        "del": null,
			"time_before": "3小时前",	
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like_count": "4",
                        "child_reply": 0
                    },
                    {
                        "id": "3",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "ccccaaa",
                        "pid": "1",
                        "reply_pid": "2",
                        "like": 0,
			"time_before": "3小时前",
                        "child_count": "0",
                        "create_time": "2019-07-31 14:29:21",
                        "update_time": null,
                        "del": null,
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like_count": "1",
                        "child_reply": 1,
                        "replied_user_id": 1,
                        "replied_nick_name": "dad2"
                    }
                ]
            },
            {
                "id": 4,
                "article_id": 58,
                "user_id": 1,
                "content": "xxxx",
                "pid": 0,
                "reply_pid": 0,
                "like": 0,
                "child_count": 0,
                "create_time": "2019-07-31 14:30:26",
                "update_time": null,
                "del": null,
                "comment_count": "4",
                "nick_name": "dad2",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                "like_count": "0",
                "child": []
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/comments?article_id=58&pid=0&per-page=2&page=1&sort=-child_count"
            }
        },
        "_meta": {
            "totalCount": 2,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 2
        }
    }
}
id 是当前评论的id
comment_count 是这篇文章的评论总数
like 是当前用户是否对这个评论点赞 1代表是
like_count 是这条评论已经被点了多少次的赞
child 是这条评论下的子评论
```  




###  添加文章评论
- 请求方式: `post`
- 请求地址: {host}`comments`
- 请求参数: 
id 文章的id
pid 3 3代表着这个评论的id 代表上级评论的id是3，如果是最顶级评论 一级评论，pid传0
```json  
{
	"id": 18,
	"content":"测试测试测试"
	"pid": "0"
}
``` 

- 响应内容:  

```json  
{
    "code": 0,
    "message": "添加成功",
    "info": ""
}

```  

###  评论点赞toggle
- 请求方式: `put`
- 请求地址: {host}`comments/18`
- 请求参数: 


- 响应内容:  

```json  
{
    "code": 0,
    "message": "添加成功",
    "active": 0
}
active 0 代表切换成未点赞的状态，1是已点赞
```  



###  评论详情
- 请求方式: `get`
- 请求地址: {host}`comment/comment-detail?id=5`
- 请求参数: 
id 评论的id


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 5,
                "article_id": 58,
                "user_id": 1,
                "content": "哈哈",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 4,
                "create_time": "2019-07-31 15:47:14",
                "update_time": null,
                "del": null,
                "comment_count": "12",
                "nick_name": "dad2",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                "like": 0,
                "like_count": "1",
                "child": [
                    {
                        "id": "6",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "好啊",
                        "pid": "5",
                        "reply_pid": "5",
                        "like_num": "0",
                        "child_count": "0",
			"time_before": "3小时前",
                        "create_time": "2019-07-31 15:47:55",
                        "update_time": null,
                        "del": null,
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like": 0,
                        "like_count": "1",
                        "child_reply": 0
                    },
                    {
                        "id": "7",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "好啊123",
                        "pid": "5",
			"time_before": "3小时前",
                        "reply_pid": "5",
                        "like_num": "0",
                        "child_count": "0",
                        "create_time": "2019-07-31 15:48:17",
                        "update_time": null,
                        "del": null,
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like": 0,
                        "like_count": "0",
                        "child_reply": 0
                    },
                    {
                        "id": "8",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "我评论7",
                        "pid": "5",
                        "reply_pid": "7",
                        "like_num": "0",
			"time_before": "3小时前",
                        "child_count": "0",
                        "create_time": "2019-07-31 15:48:35",
                        "update_time": null,
                        "del": null,
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like": 0,
                        "like_count": "0",
                        "child_reply": 1,
                        "replied_user_id": 1,
                        "replied_nick_name": "dad2"
                    },
                    {
                        "id": "9",
                        "article_id": "58",
                        "user_id": "1",
                        "content": "我评论7",
                        "pid": "5",
                        "reply_pid": "7",
			"time_before": "3小时前",
                        "like_num": "0",
                        "child_count": "0",
                        "create_time": "2019-07-31 16:41:50",
                        "update_time": null,
                        "del": null,
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-07-26/imjCmH90IdyOFBslNKk2m-jYQwv759ns.png",
                        "nick_name": "dad2",
                        "like": 0,
                        "like_count": "0",
                        "child_reply": 1,
                        "replied_user_id": 1,
                        "replied_nick_name": "dad2"
                    }
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/comment/comment-detail?id=5&child_per_page=10&child_offset_page=0&page=1"
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






###  get贷超ur;
- 请求方式: `get`
- 请求地址: {host}`general/get-dc`
- 请求参数: 


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": "http://47.103.61.179:8089/#/index"
}
```  
