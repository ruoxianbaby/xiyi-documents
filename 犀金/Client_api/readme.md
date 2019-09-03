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
    - [举报用户](./#举报用户)
    - [拉黑用户](./#拉黑用户)
- [搜索](./#搜索)
    - [文章搜索](./#文章搜索)
    - [用户搜索](./#用户搜索)
- [通用模块](./#通用模块)
	- [用户反馈](./#用户反馈)
	- [上报设备号](./#上报设备号)  
	- [上传图片接口](./#上传图片接口)
	- [get贷超url](./#get贷超url)
	- [客户端上传文件到oss](./#客户端上传文件到oss)
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
    - [举报文章](./#举报文章)
    - [专题列表](./#专题列表)
    - [专题详情](./#专题详情)    
    - [专题好文列表](./#专题好文列表)
    - [专题订阅和取消订阅](./#专题订阅和取消订阅)    
- [活动模块](./#活动模块)
    - [活动列表](./#活动列表)
    - [活动详情](./#活动详情)
    - [活动报名提交](./#活动报名提交)
    - [检测是否已经报名](./#检测是否已经报名)
    - [我的门票](./#我的门票)
- [优选模块](./#优选模块)
    - [获取新动态总个数](./#获取新动态总个数)
    - [动态列表](./#动态列表)
    - [获取新增粉丝总数](./#获取新增粉丝总数)
    - [新增粉丝列表](./#新增粉丝列表)
- [创业模块](./#创业模块)
    - [创业首页列表](./#创业首页列表)
    - [创业内页列表](./#创业内页列表)
    - [城市搜索列表](./#城市搜索列表)
    - [创业类型列表](./#创业类型列表)
    - [热门城市列表](./#热门城市列表)
    - [创业背景图列表](./#创业背景图列表)
    - [创业发布](./#创业发布)
    - [创业首页轮播图](./#创业首页轮播图)
    - [举报创业邦](./#举报创业邦)    
- [我的](./#我的)
    - [关注和昵称信息](./#关注和昵称信息)
    - [发布的文章](./#发布的文章)   
    - [我的创业邦](./#我的创业邦)   
    - [建议和反馈](./#建议和反馈)       
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

### 客户端上传文件到oss 
> 需要看阿里云的文档以及SDK
获取accessid与accesskey接口
- 请求方式: `get`
- 请求地址: {host}`generals/get-sts?client_name=client_name`
- 请求参数: client_name 客户端标识,随便传自己能分清就好
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "AccessKeySecret": "BT27qhskFeJvofZ4sq3LVgMf71WArAjCrTSdftdVe2PQ",
        "AccessKeyId": "STS.NJFWquAp6915YuszySQNhGP1K",
        "Expiration": "2019-09-03T04:42:40Z",
        "SecurityToken": "CAIS9gF1q6Ft5B2yfSjIr4nzHMvBrK8XjvPeW1PCnnkGXcFEqJWaqTz2IHlKdHduBe0XtPs0nGxU7foZlqJ4T55IQ1Dza8J148z2MdFixM+T1fau5Jko1beHewHKeTOZsebWZ+LmNqC/Ht6md1HDkAJq3LL+bk/Mdle5MJqP+/UFB5ZtKWveVzddA8pMLQZPsdITMWCrVcygKRn3mGHdfiEK00he8TontP7kn5LNu0GG1gaqlbAvyt6vcsT+Xa5FJ4xiVtq55utye5fa3TRYgxowr/4o3PIapWqW5I7GWwUNuEndKY7T6cZzIQphb6Q/GqhUQQNzf0azPYUagAGHr8Z/h1DEiA5rGioeYZpk8Cj75yFbmZ54pBLK96AjFyPGjI21qxsSV8jvxfstno9RxYIVHzIIC40+kDQeKhR0Iimvd1kfiuPDNGG5VMOaNsnZgBGcrh2RVKy77YMFz/YvjJ68c5kb/6vOrUpdIcl66hPjfWRRFxdyr/Kj68bWug=="
    }
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
type_name 文章类型
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
		"type": 1111,
		"type_name": "类型111",	
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






###  get贷超url
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



###  拉黑用户
- 请求方式: `post`
- 请求地址: {host}`user-blacklists`
- 请求参数:   
to_uid 是你要拉黑那个用户的id

```json  
{
	"to_uid":212
}
```  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": ""
}
```  



###  举报用户
- 请求方式: `post`
- 请求地址: {host}`user-reports`
- 请求参数:   
to_uid 是你要举报的那个用户的id

```json  
{
	"to_uid":212,
	"content": "没办法"
}
```  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": ""
}
```  

###  举报文章
- 请求方式: `post`
- 请求地址: {host}`article-reports`
- 请求参数:   


```json  
{
	"article_id":110,
	"content": "啊啊啊"
}
```  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": ""
}
```  


### 专题列表
- 请求方式: `get`
- 请求地址: {host}`article-types?per-page=20&page=1`
- 请求参数:  per-page 每页多少条，page 第几页


- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "at_id": 9,
                "at_name": "职场经验谈",
                "topic": "专题1",
                "topic_des": "描述1",
                "subscription_num": 112,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82107701.jpg",
                "is_sub": 0
            },
            {
                "at_id": 10,
                "at_name": "Ta的创业故事",
                "topic": "专题2",
                "topic_des": "描述2",
                "subscription_num": 111,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/96392785.jpg",
                "is_sub": 0
            },
            {
                "at_id": 11,
                "at_name": "时令新商机",
                "topic": "专题3",
                "topic_des": "描述3",
                "subscription_num": 212,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/9825760.jpg",
                "is_sub": 0
            },
            {
                "at_id": 12,
                "at_name": "创业者的自我修养",
                "topic": "专题4",
                "topic_des": "描述4",
                "subscription_num": 214,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/53568112.jpg",
                "is_sub": 0
            },
            {
                "at_id": 13,
                "at_name": "大神设计",
                "topic": "专题5",
                "topic_des": "描述5",
                "subscription_num": 132,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/87280608.jpg",
                "is_sub": 0
            },
            {
                "at_id": 14,
                "at_name": "投资指南",
                "topic": "专题6",
                "topic_des": "描述6",
                "subscription_num": 177,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/54815439.jpg",
                "is_sub": 0
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/article-types?page=1"
            }
        },
        "_meta": {
            "totalCount": 6,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
"at_id": 9 专题好文列表的id   is_sub是否订阅 1代表已经订阅
```


### 专题好文列表
- 请求方式: `get`
- 请求地址: {host}`articles?type=12`
- 请求参数:  type=12 的12对应的是专题列表的 at_id


- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
		{
                "id": 58,
                "type": 12,
                "origin": "开始吧",
                "author": "阿军",
                "title": "开赚钱的咖啡店，你必须知道这7件事",
                "desc": "开一家咖啡店并不是个容易的事",
                "profile": null,
                "preview_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/05b93d90b5b94b71a5dd8020587f33c6.jpeg",
                "comment_num": "6",
                "like_num": "1",
                "create_time": "2019-07-23 16:51:01",
                "update_time": "2019-08-09 14:02:24",
                "creater": 110,
                "admin_id": 92,
                "status": 1,
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/72429149.jpg",
                "type_name": "创业者的自我修养",
                "preview_content": "<p>想来也是，在步履匆匆的生活节奏下，咖啡馆打包了大多数人想要的「理想生活」的样子：阳光、咖啡、绿植、书本、慢时光......可以和喜欢的一切在一起。但眼看着街角的咖啡店，一年换了好几块招牌，梦想到梦想破灭的距",
                "before_time": "34天前",
                "share_url": "http://47.103.61.179:8084",
                "like": 0,
                "focus": 0,
                "collect_num": "1",
                "collect": 0,
                "img_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/05b93d90b5b94b71a5dd8020587f33c6.jpeg"
            },
	      {
                "id": 70,
                "type": 12,
                "origin": "信合企业服务平台",
                "author": "刻苦铭心",
                "title": "创业千万条，商标是头条",
                "desc": "商标保护的重要性",
                "profile": null,
                "preview_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%287%29.jpg",
                "comment_num": 0,
                "like_num": "0",
                "create_time": "2019-07-24 12:29:25",
                "update_time": "2019-08-09 14:08:09",
                "creater": 124,
                "admin_id": 92,
                "status": 1,
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/18889273.jpg",
                "type_name": "创业者的自我修养",
                "preview_content": "<p class=\"ql-align-justify\">商标其于企业，如名字之于人，起步之初或只是形象，但是随着企业的发展商标的重要性也日益凸显，尤其在当前经济形势下企业之间竞争加剧，商标就更显得举足轻重了。</p><p class=\"ql-align-justify\"><br></p><p c",
                "before_time": "33天前",
                "share_url": "http://47.103.61.179:8084",
                "like": 0,
                "focus": 0,
                "collect_num": "0",
                "collect": 0,
                "img_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%287%29.jpg"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/article-types?page=1"
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
"at_id": 9 专题好文列表的id
```



### 专题订阅和取消订阅
- 请求方式: `post`
- 请求地址: {host}`article-type-subscription/toggle`
- 请求参数:  
```json
{
	"article_type_id":12
}
```


- 响应内容:  
```json
{
    "code": 1,
    "message": "切换成功",
    "info": {
        "is_sub": 0
    }
}
1代表切换成了订阅状态 0代表切换成了未订阅状态
```



### 专题详情
- 请求方式: `get`
- 请求地址: {host}`article-types/11`
- 请求参数:  


- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "at_id": 11,
                "at_name": "时令新商机",
                "topic": "专题3",
                "topic_des": "描述3",
                "subscription_num": 212,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/9825760.jpg",
                "is_sub": 0
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/article-types/11?page=1"
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


###  活动列表
- 请求方式: `get`
- 请求地址: {host}`activities`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "title": "标题",
                "location": "上海",
                "price": "1333.33",
                "user_id": 155,
                "preview_image": "",
                "activity_time": "2019-08-12",
                "registration_deadline": "2019-08-12 10:57:38",
                "is_free": 1,
                "creater_name": "琪琪男孩",
                "activity_time_end": "2019-08-14"
            },
            {
                "id": 2,
                "title": "标题222",
                "location": "北京",
                "price": "1222.00",
                "user_id": 156,
                "preview_image": "",
                "activity_time": "2019-08-12",
                "registration_deadline": "2019-08-12 13:17:28",
                "is_free": 1,
                "creater_name": "Release my soul",
                "activity_time_end": "2019-08-16"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/activities?page=1"
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
is_free 1代表是免费的
registration_deadline 报名截止日期
activity_time 活动开始日期
activity_time_end 活动end日期
```  

###  活动详情
- 请求方式: `get`
- 请求地址: {host}`activities/1?expand=content,item`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "title": "标题",
                "location": "上海",
                "price": "1333.33",
                "user_id": 155,
                "preview_image": "",
                "activity_time": "2019-08-12",
                "registration_deadline": "2019-08-12 10:57:38",
                "is_free": 1,
                "creater_name": "琪琪男孩",
                "activity_time_end": "2019-08-14",
                "content": "内容内容内容内容内容内容内容内容内容"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/activities/1?expand=content%2Citem&page=1"
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
content 活动详情内容
item 活动报名时候报名的项目
	is_register 报过名就是1，报过名的不能再次报名活动项目
```  



###  活动报名提交
- 请求方式: `post`
- 请求地址: {host}`activities`
- 请求参数:   
```json  
{
	"activity_id": 3,
	"mobile": 123,
	"name": "feixiang",
	"price": 123.00
}
```  


- 响应内容:  

```json  

```  



###  检测是否已经报名
- 请求方式: `post`
- 请求地址: {host}`activity-item-sign-up/check-register`
- 请求参数:   
```json  
{
	"activity_id": 3,
}
```  


- 响应内容:  

```json  
{
    "code": 0,
    "message": "已经报名过该项目",
    "info": {
        "is_register": true
    }
}
```  



###  我的门票
- 请求方式: `get`
- 请求地址: {host}`activity-item-sign-up/my-ticket?activity=3`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "获取成功",
    "info": {
        "id": "3",
        "title": "标题",
        "location": "上海",
        "price": "133.00",
        "preview_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/59081007160c1.jpg",
        "activity_time": "2019-08-12 17:19:07",
        "activity_time_end": "2019-08-12 17:19:09",
        "is_free": "1",
        "mobile": "13636655412",
        "user_name": "微微笑"
    }
}
```  

###  获取新动态总个数
- 请求方式: `get`
- 请求地址: {host}`message-dynamic/new-dynamic-num`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "new_dynamic_num": 2
    }
}
```  


###  动态列表
- 请求方式: `get`
- 请求地址: {host}`message-dynamic/get-dynamic`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "操作成功",
    "info": [
        {
            "user_id": "4",
            "type": "2",
            "create_time": "1小时前",
            "content": "内容123",
            "article_comment_id": "200",
            "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/72024891.jpg",
            "nick_name": "梦太阳",
            "info": "我真的一个人去吃过火锅，好像也没那么让人难以接受",
            "article_id": "543",
            "article_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-08-19/ZM6ERzrqZfUS-yRmogiEoeLCBfjABsz1.jpg"
        },
        {
            "user_id": "3",
            "type": "1",
            "create_time": "1小时前",
            "content": "内容5555",
            "article_comment_id": "65",
            "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg",
            "nick_name": "时光偏执",
            "info": "葡萄酒投资回报超股票黄金",
            "article_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/d5269bf3cf144969aecb2546393421cc_th.jpg",
            "article_id": "65"
        }
    ]
}
```  

###  获取新增粉丝总数
- 请求方式: `get`
- 请求地址: {host}`get-fans-num`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "获取成功",
    "info": {
        "new_fans_num": 0
    }
}
```  

###  新增粉丝列表
- 请求方式: `get`
- 请求地址: {host}`focu/new-fans-list?per-page=2&page=1`
- 请求参数:   per-page 和 page都是分页参数，可以不传


- 响应内容:  

```json  
{
    "code": 1,
    "message": "获取成功",
    "info": {
        "items": [
            {
                "read": 0,
                "nick_name": "多啦A梦",
                "fans_id": 166
            },
            {
                "read": 0,
                "nick_name": "阿军",
                "fans_id": 110
            }
        ],
        "_meta": {
            "totalCount": 2,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 2
        }
    }
}
```  
## 创业模块

### 城市搜索列表
- 请求方式: `get`
- 请求地址: {host}`cities?name=`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 310000,
                "name": "上海市",
                "pid": 86
            },
            {
                "id": 361100,
                "name": "江西省·上饶市",
                "pid": 360000
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/city/list?name=%E4%B8%8A&page=1"
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

### 热门城市列表
- 请求方式: `get`
- 请求地址: {host}`city/popular-list?limit=`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": "460000",
                "name": "海南省",
                "count": "2"
            },
            {
                "id": "110000",
                "name": "北京市",
                "count": "2"
            },
            {
                "id": "650000",
                "name": "新疆维吾尔自治区",
                "count": "1"
            },
            {
                "id": "320000",
                "name": "江苏省",
                "count": "1"
            },
            {
                "id": "710000",
                "name": "台湾省",
                "count": "1"
            }
        ]
    }
}
```

### 创业类型列表
- 请求方式: `get`
- 请求地址: {host}`business-types`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "name": "求县令",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg"
            },
            {
                "id": 2,
                "name": "求资金",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg"
            },
            {
                "id": 3,
                "name": "求方案",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg"
            },
            {
                "id": 4,
                "name": "约个饭",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg"
            },
            {
                "id": 5,
                "name": "其他活动",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/business-types?page=1"
            }
        },
        "_meta": {
            "totalCount": 5,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```

### 创业背景图列表
- 请求方式: `get`
- 请求地址: {host}`business-backgrounds`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
            },
            {
                "id": 2,
                "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
            },
            {
                "id": 3,
                "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
            },
            {
                "id": 4,
                "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
            },
            {
                "id": 5,
                "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/business-backgrounds?page=1"
            }
        },
        "_meta": {
            "totalCount": 5,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```

### 创业发布
- 请求方式: `post`
- 请求地址: {host}`businesses`
- 请求参数:  
```json
{
    "b_id": "创业背景图列表id",
    "c_id": "城市搜索列表id",
    "t_id": "创业类型列表id",
    "area": "领域",
    "end_time": "结束时间 e.g. 2019-09",
    "description": "描述",
    "pics": [ 
	"https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg",
	"https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
    ]
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "b_id": 1,
        "c_id": 1,
        "t_id": 1,
        "area": "领域",
        "end_time": "2019-09",
        "description": "描述",
        "id": 1
    }
}
```

### 创业首页列表
- 请求方式: `get`
- 请求地址: {host}`businesses`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 4,
                "u_id": 4,
                "b_id": 1,
                "c_id": 370200,
                "t_id": 1,
                "area": "领域",
                "description": "描述",
                "interested_nums": 0,
                "create_time": "2019-08-26 16:59:59",
                "update_time": "2019-08-27 10:57:00",
                "end_time": "0000-00-00",
                "status": 1,
                "is_del": 0,
                "type_name": "求县令",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/72024891.jpg",
                "city_name": "青岛市",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
            },
            {
                "id": 3,
                "u_id": 3,
                "b_id": 1,
                "c_id": 321300,
                "t_id": 1,
                "area": "领域",
                "description": "描述",
                "interested_nums": 0,
                "create_time": "2019-08-26 16:59:41",
                "update_time": "2019-08-27 10:57:00",
                "end_time": "0000-00-00",
                "status": 1,
                "is_del": 0,
                "type_name": "求县令",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg",
                "city_name": "宿迁市",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/businesses?sort=-id&page=3&per-page=2"
            },
            "first": {
                "href": "http://xj.org/businesses?sort=-id&page=1&per-page=2"
            },
            "prev": {
                "href": "http://xj.org/businesses?sort=-id&page=2&per-page=2"
            },
            "next": {
                "href": "http://xj.org/businesses?sort=-id&page=4&per-page=2"
            },
            "last": {
                "href": "http://xj.org/businesses?sort=-id&page=4&per-page=2"
            }
        },
        "_meta": {
            "totalCount": 8,
            "pageCount": 4,
            "currentPage": 3,
            "perPage": 2
        }
    }
}
```

### 创业内页列表
- 请求方式: `get`
- 请求地址: {host}`business/list`
- 请求参数:  
id 首页列表id  
t_id 首页列表t_id || 主题搜索列表id  
c_id 地点搜索列表id  
end_time 截止时间  
page  per-page

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": "1",
                "u_id": "1",
                "b_id": "1",
                "c_id": "110106",
                "t_id": "1",
                "area": "领域",
                "description": "描述",
                "interested_nums": "0",
                "create_time": "2019-08-26 16:47:01",
                "update_time": "2019-08-27 11:09:30",
                "end_time": "-0001年11月",
                "status": "1",
                "is_del": "0",
                "pic_list": [
                    "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg",
                    "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
                ],
                "nick_name": "智能机器人",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "city_name": "丰台区"
            },
            {
                "id": "6",
                "u_id": "6",
                "b_id": "1",
                "c_id": "653000",
                "t_id": "1",
                "area": "领域",
                "description": "描述",
                "interested_nums": "0",
                "create_time": "2019-08-26 17:00:22",
                "update_time": "2019-08-27 10:57:00",
                "end_time": "2019年09月",
                "status": "1",
                "is_del": "0",
                "pic_list": [
                    "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg",
                    "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
                ],
                "nick_name": "啊哒嘀",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/32240700.jpg",
                "city_name": ""
            }
        ],
        "_meta": {
            "totalCount": 2,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```

### 创业首页轮播图
- 请求方式: `get`
- 请求地址: {host}`business-banners?sort=-id`  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 3,
                "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg",
                "web_url": "http://www.baidu.com"
            },
            {
                "id": 2,
                "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg",
                "web_url": "http://www.baidu.com"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/business-banners?sort=-id&page=1"
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



### 举报创业邦
- 请求方式: `post`
- 请求地址: {host}`business-reports`
- 请求参数:  
```json
{
	"business_id": 1,
	"content": "非法的东西"
}
```

- 响应内容:  
```json
{
    "code": 1,
    "message": "创建成功",
    "info": {
        "business_id": 1,
        "content": "非法的东西",
        "user_id": 1,
        "id": 3
    }
}
```



### 关注和昵称信息
- 请求方式: `get`
- 请求地址: {host}`my-center/get-focus-info`
- 请求参数:  

- 响应内容:  
```json
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "focus_num": 3,
        "focused_num": 2,
        "nick_name": "智能机器人",
        "mobile": "150****0110",
        "gender": "男",
        "city_name": "北京市东城区"
    }
}
foucus_num关注数，focused_num被关注数
```




### 发布的文章
- 请求方式: `get`
- 请求地址: {host}`articles?my=1&page=1&per-page=3`
- 请求参数:  articles?my=1是写死的，后面的参数代表page=1第一页,per-page显示3条

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 58,
                "title": "开赚钱的咖啡店，你必须知道这7件事",
                "comment_num": 6,
                "like_num": "1",
                "create_time": "2019-07-23 16:51:01",
                "update_time": "2019-08-09 14:02:24",
                "type_name": "创业者的自我修养"
            },
            {
                "id": 61,
                "title": "为什么说创业就像谈恋爱",
                "comment_num": 5,
                "like_num": "1",
                "create_time": "2019-07-24 10:09:47",
                "update_time": "2019-08-09 14:03:06",
                "type_name": "Ta的创业故事"
            },
            {
                "id": 62,
                "title": "聪明投资者的预期收益",
                "comment_num": 0,
                "like_num": "0",
                "create_time": "2019-07-24 10:27:34",
                "update_time": "2019-08-09 14:03:55",
                "type_name": "投资指南"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/articles?my=1&page=1&per-page=3"
            },
            "next": {
                "href": "http://my_xijin_api.com/articles?my=1&page=2&per-page=3"
            },
            "last": {
                "href": "http://my_xijin_api.com/articles?my=1&page=2&per-page=3"
            }
        },
        "_meta": {
            "totalCount": 4,
            "pageCount": 2,
            "currentPage": 1,
            "perPage": 3
        }
    }
}
```





### 我的创业邦
- 请求方式: `get`
- 请求地址: {host}`businesses?u_id=1`
- 请求参数:  uid,用户id

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 8,
                "u_id": 1,
                "b_id": 1,
                "c_id": 460300,
                "t_id": 1,
                "area": "领域",
                "description": "描述",
                "interested_nums": 0,
                "create_time": "2019-08-27 10:57:48",
                "update_time": "2019-08-28 15:10:42",
                "end_time": "2019-09-01",
                "status": 1,
                "is_del": 0,
                "type_name": "求贤令",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "city_name": "三沙市",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/oN2NdUF4ggE1gwDMXUzzPg2VXDWKKB62.jpg",
                "type_logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/ir5S-RuAcVb-3v_uME1zHkWWdhhQkTCK.png"
            },
            {
                "id": 7,
                "u_id": 1,
                "b_id": 1,
                "c_id": 710000,
                "t_id": 2,
                "area": "领域",
                "description": "描述",
                "interested_nums": 0,
                "create_time": "2019-08-27 10:54:41",
                "update_time": "2019-08-27 18:00:19",
                "end_time": "2019-09-01",
                "status": 1,
                "is_del": 0,
                "type_name": "求资金",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "city_name": "台湾省",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/oN2NdUF4ggE1gwDMXUzzPg2VXDWKKB62.jpg",
                "type_logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/_gL9-fmosnl7MXWacQ2GCnfuUfyE75_h.png"
            },
            {
                "id": 1,
                "u_id": 1,
                "b_id": 1,
                "c_id": 110106,
                "t_id": 1,
                "area": "领域",
                "description": "描述",
                "interested_nums": 0,
                "create_time": "2019-08-26 16:47:01",
                "update_time": "2019-08-29 17:28:55",
                "end_time": "2019-08-29",
                "status": 1,
                "is_del": 0,
                "type_name": "求贤令",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "city_name": "丰台区",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/oN2NdUF4ggE1gwDMXUzzPg2VXDWKKB62.jpg",
                "type_logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/ir5S-RuAcVb-3v_uME1zHkWWdhhQkTCK.png"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/businesses?u_id=1&page=1"
            }
        },
        "_meta": {
            "totalCount": 3,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```




### 建议和反馈
- 请求方式: `post`
- 请求地址: {host}`suggestions`
- 请求参数:  
```json
{
	"content":"反馈的内容",
	"mobile": "联系人手机 可选的",
	"email": "联系人邮箱 也是可选的"
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "content": "反馈的内容",
        "mobile": "联系人手机 可选的",
        "email": "联系人邮箱 也是可选的",
        "user_id": 1,
        "id": 3
    }
}
```
