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
    - [检查重复手机号](./#检查重复手机号)   
- [搜索](./#搜索)
    - [综合搜索](./#综合搜索) 
    - [文章搜索](./#文章搜索)
    - [用户搜索](./#用户搜索)
    - [电台搜索](./#电台搜索)   
    - [创业邦搜索](./#创业邦搜索)  
- [通用模块](./#通用模块)
	- [用户反馈](./#用户反馈)
	- [上报设备号](./#上报设备号)  
	- [上传图片接口](./#上传图片接口)
	- [get贷超url](./#get贷超url)
	- [客户端上传文件到oss](./#客户端上传文件到oss)
	- [检测手机号](./#检测手机号)  
	- [ios审核](./#ios审核)
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
    - [通知数](./#通知数)
    - [通知列表](./#通知列表)    
    - [动态列表](./#动态列表)
    - [新增粉丝列表](./#新增粉丝列表)
    - [更新设备device_tokens](./#更新设备device_tokens) 
    - [通知透传](./#通知透传)   
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
    - [和我聊聊](./#和我聊聊)    
- [我的](./#我的)
    - [信息](./#信息)
    - [发布的文章](./#发布的文章)   
    - [我的创业邦](./#我的创业邦)
    - [我的订阅](./#我的订阅)     
    - [通知消息设置](./#通知消息设置)    
    - [建议和反馈](./#建议和反馈)    
    - [编辑个人资料](./#编辑个人资料)
    - [关注作者](./#关注作者)  
    - [ta的关注和粉丝](./#ta的关注和粉丝)       
- [电台](./#电台)
    - [电台列表](./#电台列表)
    - [电台列表详情](./#电台列表详情)    
    - [电台点赞](./#电台点赞)
    - [电台收藏](./#电台收藏)    
    - [电台列表内页的评论](./#电台列表内页的评论)     
    - [电台最新评论](./#电台最新评论)     
    - [电台最热评论](./#电台最热评论)         
    - [电台评论详情](./#电台评论详情)   
    - [电台评论点赞](./#电台评论点赞)        
    - [电台post评论](./#电台post评论)
    - [电台举报](./#电台举报)     
    - [电台时间轴](./#电台时间轴)   
    - [电台banner](./#电台banner)   
    - [我的电台](./#我的电台)  
    - [电台标题搜索](./#电台标题搜索)
    - [电台评论个数](./#电台评论个数)    
- [赚钱圈](./#赚钱圈)
    - [领域列表](./#领域列表)
    - [圈子创建](./#圈子创建)    
    - [圈子修改](./#圈子修改)
    - [圈子信息](./#圈子信息)    
    - [圈子删除](./#圈子删除)      
    - [圈子列表](./#圈子列表)      
    - [聊天点赞](./#聊天点赞)      
    - [聊天点赞查询](./#聊天点赞查询)      
    - [根据第三方用户id查询用户信息](./#根据第三方用户id查询用户信息)      
    - [圈子成员新增](./#圈子成员新增)      
    - [圈子成员删除](./#圈子成员删除)      
    - [圈子成员列表](./#圈子成员列表)      
    - [用户信息查询](./#用户信息查询)          
    - [名片列表](./#名片列表)              
    - [名片新增](./#名片新增)         
    - [名片修改](./#名片修改)         
    - [名片删除](./#名片删除)         
    - [更改群主](./#更改群主)         
    - [小报当日数量统计](./#小报当日数量统计)         
    - [小报列表](./#小报列表)         
    - [赚钱圈banner](./#赚钱圈banner)         
    - [赚钱圈圈子信息](./#赚钱圈圈子信息)         
    - [个人中心我/他的圈子](./#个人中心我/他的圈子)         

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
> 参数说明: 拼接上`?expand=today-browse,total-browse,focus,article_count` 可查看今日和总浏览数,关注数, 发表文章数
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

### 综合搜索
- 请求方式: `get`
- 请求地址: {host}`searches?keyword=我`

- 响应内容:  
```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "radio_data": [
            {
                "id": "2",
                "title": "我为什么要“做人留一线”？聊一聊生活在一线城市的利与弊",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-10-17/mDOyRKbP1FyrgblUPHPMhlCBhi4zal7t.png"
            }
        ],
        "business_data": [
            {
                "id": "110",
                "area": "共享充电宝",
                "description": "搞共享充电宝的有兴趣+，产品开发已经成熟，广告已接好，找地推，各个城市分开推广，我们提供设备和服务，客户你来布局。我们是按照你开的客户的使用情况分成的，做得好真的可以躺着赚钱。有兴趣聊一下",
                "type_name": "求贤令",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-09-18/ZpZS4rgGmkxl0d8gvu5iwTKYUIl_Bb1Q.jpg",
                "city_name": "苏州市"
            },
            {
                "id": "108",
                "area": "跨境代购",
                "description": "招微商下游，有没有想做澳洲代购的，提供澳洲直邮批发的货源！可以帮忙代发，提供全程服务。你只要给我订单，我帮你解决一切，有意私聊",
                "type_name": "求贤令",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-09-18/Bd2bjy-Qv7GTimEUgh9hYiUjheqb1WI1.jpg",
                "city_name": "上海市"
            },
            {
                "id": "104",
                "area": "淘宝卖家",
                "description": "我是开淘宝店的，卖食品，三钻，一直收益平平，推广太烧钱了，感觉再给马云打工。有么有大佬能指条明路",
                "type_name": "求方案",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-09-02/inkutBskMs5ys8xy41GqAFKWt8PMOXri.png",
                "city_name": "四川省"
            },
            {
                "id": "100",
                "area": "软件工程",
                "description": "公司已开，坐标深圳，主要从事原创Vtuber行业，现在已经在B站开号并获取了一定的流量。公司需要一个靠谱的Unity程序员实现动态捕捉设备和Unity引擎的连接，实现直播。我们理念非常新颖，发张实拍，B站号：Facemoe，有意者欢迎私聊",
                "type_name": "求贤令",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-09-18/PyvV0rS39k6ty2NHp2_fw1iz0IIrvKfM.jpg",
                "city_name": "深圳市"
            },
            {
                "id": "5",
                "area": "互联网Vtuber",
                "description": "公司已开，坐标深圳，主要从事原创Vtuber行业，现在已经在B站开号并获取了一定的流量。可出让60%股份，求融资，300万元。公司主打Mixed Reality Idol，这个概念在中国是首创。有兴趣欢迎看我们B站号：Facemoe",
                "type_name": "求资金",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/KNYnpWCwtGPyCsni30ZoVcoouQGukTGi.jpg",
                "city_name": "深圳市"
            },
            {
                "id": "4",
                "area": "私域电商",
                "description": "和阿里合作的新项目，是做的私域电商平台+供应链，目前再招城市合伙人，我们公司提供系统，功能是可以帮助所有想再线上卖货的商家搭建属于商家自己的小taobao平台，并提供一个丰富的货源，我们来做线上推广，合伙人做线下推广，可以baidu美物满仓",
                "type_name": "求贤令",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-09-18/Bd2bjy-Qv7GTimEUgh9hYiUjheqb1WI1.jpg",
                "city_name": "成都市"
            }
        ],
        "article_data": [
            {
                "id": "928",
                "title": "我们都小看了周杰伦的带货能力",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-09-18/3_9ew8wBix25izH8E-mKq2dalUDz4cl6.jpg",
                "type": "12",
                "like_num": "21",
                "type_name": "创业者的自我修养"
            },
            {
                "id": "917",
                "title": "二十多通电话后，我摸清了加盟奶茶店的这些坑",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-09-17/VadpVfpGSy2OMS4iv9dbB3F3S4dJ3rNK.jpg",
                "type": "12",
                "like_num": "42",
                "type_name": "创业者的自我修养"
            },
            {
                "id": "912",
                "title": "日本老龄化消费调研：哪类产品更好卖？有哪些值得我们借鉴",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-09-17/1vx-ikns4tsvO-whlj0KK4n9ANuaZjpr.jpg",
                "type": "14",
                "like_num": "41",
                "type_name": "投资指南"
            }
        ],
        "user_data": [
            {
                "id": "15",
                "nick_name": "深伴我",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/9825760.jpg",
                "focus_num": "1",
                "product_num": "2"
            },
            {
                "id": "18",
                "nick_name": "醉友我",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/13742375.jpg",
                "focus_num": "1",
                "product_num": "5"
            },
            {
                "id": "37",
                "nick_name": "顾及我",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/90135688.jpg",
                "focus_num": "0",
                "product_num": "4"
            }
        ],
	"group_data": [
            {
                "name": "嗯",
                "description": "男女皆可",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-11-19/mFc57bZa84qSO5HM7_MmChUA9RX3O6lf.png",
                "nums": 1,
                "upvote_nums": 0,
                "im_group_id": 99343851913217,
                "create_time": "2019-11-19 13:08:00",
                "is_new": 1,
                "join_status": 0
            },
            {
                "name": "嗯",
                "description": "男女皆可",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-11-19/mFc57bZa84qSO5HM7_MmChUA9RX3O6lf.png",
                "nums": 1,
                "upvote_nums": 0,
                "im_group_id": 99343825698817,
                "create_time": "2019-11-19 13:07:45",
                "is_new": 1,
                "join_status": 0
            },
            {
                "name": "嗯",
                "description": "女款",
                "logo": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-11-19/S-YCzgFfvi1-4HapB9iXQBEaJDm2zdNl.png",
                "nums": 1,
                "upvote_nums": 0,
                "im_group_id": 99339510808578,
                "create_time": "2019-11-19 11:59:00",
                "is_new": 1,
                "join_status": 0
            }
        ]
    }
}
电台和创业邦最多反了6条数据，文章和犀客最多返了3条数据， 查看更多调另外的搜索接口。
```


### 用户搜索
- 请求方式: `get`
- 请求地址: {host}`users?nick_name=da`
> 参数 `nick_name=da` 模糊搜索  
> 拼接上`?expand=today-browse,total-browse,focus,article_count` 可查看今日和总浏览数,关注数, 发表文章数
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


### 电台搜索
- 请求方式: `get`
- 请求地址: {host}`radios?title=%要搜索的内容%`
- 请求参数: 直接把要搜索的内容传递到参数上

```json

```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 7,
                "radio_url": "http://xijin-test.oss-cn-shanghai.aliyuncs.com/radio/2019-10-15/1571132739853.mp3",
                "size": "88393.52",
                "type": 0,
                "origin": "",
                "title": "低成本创业是不是一个伪命题？",
                "desc": "孤注一掷的勇气究竟能否开花结果",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-10-18/xNL52KR6FJCKxzw4JjyMkXtE75a66J0L.png",
                "comment_num": 0,
                "like_num": 25,
                "create_time": "2019-10-15",
                "before_time": "5天前",
                "like": 0,
                "collect_num": 0,
                "collect": 0,
                "share_url": "http://my_xijin_api.com/?id=7&radio_url=http://xijin-test.oss-cn-shanghai.aliyuncs.com/radio/2019-10-15/1571132739853.mp3",
                "radio_time": "36:58",
                "radio_size": "86.32MB",
                "participants": [
                    {
                        "id": 121,
                        "nick_name": "主页菌",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-27/Am7n0XLBqZ_Pffl1JJhgHzf9mCltG_79.png"
                    },
                    {
                        "id": 227,
                        "nick_name": "Ծ‸Ծ",
                        "avatar_image": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTLRbCnyAoRJV6QbTeOicKR3icGsNIxgfkqu6b9Zf4a7ViaVECzzianqFcqPxTRyzLVynlkgRdueibZO7nQ/132"
                    },
                    {
                        "id": 374,
                        "nick_name": null,
                        "avatar_image": null
                    }
                ],
                "radio_shaft": [
                    {
                        "id": 204,
                        "radio_id": 7,
                        "at": 38,
                        "title": "本期内容",
                        "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-10-18/UrqvpKCnfpdA7vzKMJSCC-Rg77bY7oyf.png",
                        "content": "低成本创业有多难，本期节目我们跟大家聊一聊这个话题。很多时候不一定是创业思路不对，只是在最艰难的时候，没有资金会让你力不从心。",
                        "quote_href": ""
                    }
                  
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radios?title=%E4%BD%8E%E6%88%90%E6%9C%AC&page=1"
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
### 创业邦搜索
- 请求方式: `get`
- 请求地址: {host}`businesses?description=我`
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
- 请求地址: {host}`general/get-sts?client_name=client_name`
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
### 检测手机号
> 先调用发送验证码接口
- 请求方式: `post`
- 请求地址: {host}`user/check-mobile`
- 请求参数: 
```json
{
	"mobile": 15061690110,
	"sms_code": 5525
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

### ios审核
- 请求方式: `post`
- 请求地址: {host}`generals/fskj`
- 请求参数: 
```json
{
	"noisrev": 1
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
- 请求地址: {host}`articles?page=1&per-page=20`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
    	    {
            "id": 983,
            "type": 9,
            "origin": "管理的常识",
            "author": "沉沦",
            "title": "遇到会做这5项工作的内部导师，一定要珍惜",
            "desc": "必须要明白“渡人渡己”的道理",
            "profile": null,
            "premium": 0,
            "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-09-25/CwBqchQagJ7y6O8nn7PAIteOn18h2o_c.jpg",
            "comment_num": "2",
            "like_num": "25",
            "create_time": "2019-09-25",
            "update_time": null,
            "creater": 41,
            "admin_id": null,
            "status": 1,
            "type_status": 1,
            "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/86023080.jpg",
            "type_name": "职场经验谈",
            "preview_content": "<p class=\"ql-align-justify\"><strong>01&nbsp;优秀职场导师，乃企业之幸</strong></p><p class=\"ql-align-justify\"><br></p><p class=\"ql-align-justify\">华为公司是国内最早实施内部导师制，且获得极大成功的企业之一。但众多企业纷纷仿效之后，却发现有效?",
            "before_time": "74天前",
            "share_url": "https://api.xykj1.com/share",
            "like": 0,
            "focus": 0,
            "collect_num": "1",
            "collect": 0,
            "img_url": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-09-25/CwBqchQagJ7y6O8nn7PAIteOn18h2o_c.jpg"
     	    },
	    {
            "at_id": "11",
            "at_name": "时令新商机",
            "topic": "专题3",
            "topic_des": "洞察各行各业的机会与挑战，找准风口，做飞的最高的那只风筝",
            "subscription_num": "214",
            "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/others/2019-09-12/ktY8nx5yPO_KM2QCwIR8z99YswO6uHgv.png",
            "weight": "0",
            "is_del": "0",
            "type_status": 2
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
type_status 1 文章   2是专题

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

###  检查重复手机号
- 请求方式: `post`
- 请求地址: {host}`general/check-repeat-mobile`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 0,
    "message": "手机号没有重复",
    "info": {
        "status": 1
    }
}
1 手机号没有重复
0 手机号有重复
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


###  通知列表
- 请求方式: `get`
- 请求地址: {host}`inform-dynamics?page=1&per-page=20`
- 请求参数:   page=1&per-page=20是分页参数


- 响应内容:  

```json  
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "items": [
            {
                "id": "1",
                "dc_id": "3",
                "url": "https://www.baidu.com",
                "title": "金枪鱼借钱",
                "icon": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/%E9%A6%96%E9%A1%B511.png",
                "desc": "描述",
                "create_time": "2019-09-12 11:07:24",
                "read": 1
            },
            {
                "id": "2",
                "dc_id": "22",
                "url": "https://www.baidu.com",
                "title": "红烧肉贷款",
                "icon": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%286%29.jpg",
                "desc": "描述",
                "create_time": "2019-09-12 11:07:34",
                "read": 1
            },
            {
                "id": "3",
                "dc_id": "11",
                "url": "https://www.baidu.com",
                "title": "代上钱包",
                "icon": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20190802112834.jpg",
                "desc": "描述",
                "create_time": "2019-09-12 11:12:06",
                "read": 1
            },
            {
                "id": "4",
                "dc_id": "12",
                "url": "https://www.baidu.com",
                "title": "测试产品",
                "icon": "",
                "desc": "测试产品测试推送",
                "create_time": "2019-09-12 11:27:44",
                "read": 1
            },
            {
                "id": "5",
                "dc_id": "123",
                "url": "https://www.baidu.com",
                "title": "123",
                "icon": "https://xijin.oss-cn-shanghai.aliyuncs.com/others/2019-09-12/QC4VD1hft5zfwcZZnqBnKTKhMKWAbE-r.jpg",
                "desc": "123123",
                "create_time": "2019-09-12 11:29:24",
                "read": 1
            }
        ],
        "_meta": {
            "totalCount": 5,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}

```  

###  动态列表
- 请求方式: `get`
- 请求地址: {host}`message-dynamic/get-dynamic?page=1&per-page=10`
- 请求参数:   page=1&per-page=10 第一页显示10条


- 响应内容:  

```json  
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "items": [
            {
                "user_id": "4",
                "type": "2",
                "create_time": "14天前",
                "content": "内容123",
                "article_comment_id": "200",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/72024891.jpg",
                "nick_name": "梦太阳",
                "info": "我真的一个人去吃过火锅，好像也没那么让人难以接受",
		"read": 0,	
                "article_id": "543",
                "article_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-08-19/ZM6ERzrqZfUS-yRmogiEoeLCBfjABsz1.jpg",
		 "top_comment_id": "459"
            },
            {
                "user_id": "3",
                "type": "1",
                "create_time": "14天前",
                "content": "内容5555",
                "article_comment_id": "65",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/64194272.jpg",
                "nick_name": "时光偏执",
                "info": "葡萄酒投资回报超股票黄金",
		"read": 0,
                "article_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/d5269bf3cf144969aecb2546393421cc_th.jpg",
                "article_id": "65",
		"top_comment_id": "459"
            }
        ],
        "_meta": {
            "totalCount": 2,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 10
        }
    }
}
read 0 未读, 1已读
type 1 文章    2 评论
user_id  谁回复了你的评论/  评论了你的文章  评论者的id
article_comment_id 评论的id
info  xxx回复了你的评论yyyy     yyyy就是info  就是回复了你什么的评论 /文章
content 回复评论的内容 / 评论文章的内容
top_comment_id  评论的id，用于调用comment/comment-detail?id=460 评论详情的接口
nick_name 回复了 info ： content
nick_name 评论了 info ： content
```  

###  通知数
- 请求方式: `get`
- 请求地址: {host}`message-dynamic/new-dynamic-num`
- 请求参数:   


- 响应内容:  

```json  
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "inform_num": 0,
        "dynamic_num": 0,
        "new_fans_num": 0
    }
} 
inform_num 通知数，  dynamic_num 动态数，  new_fans_num 粉丝数
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
                "nick_name": "多啦A梦",
                "fans_id": 166,
		"read": 0	
            },
            {
                "nick_name": "阿军",
                "fans_id": 110,
		"read":0
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
read 0 未读
```  


###  更新设备device_tokens
- 请求方式: `post`
- 请求地址: {host}`general/set-device-tokens`
- 请求参数: 

```json  
{
	"user_id": 2,
	"type": 1,
	"device_tokens": "安卓或ios的一长串token"
}
type 1是安卓，2是IOS
```  


- 响应内容:  

```json  
{
    "code": 1,
    "message": "操作成功",
    "info": ""
}
```  


###  通知透传
- 请求方式: `get`
- 请求地址:  可以评论文章或者回复他人评论
- 请求参数:  


- 响应内容:  

```json  
{
    "type": 2,
    "nick_name": "微微笑",
    "article_comment_id": "403",
    "article_comment_info": "融资方面 还是需要有经验的人帮忙扶持下",
    "content": "还不错"
}
nick_name 回复了 article_comment_info ： content
type 1和2数据格式返回一致
type 1 是评论了文章
type 2 是回复了评论
```  
- type=4是新增的粉丝推送 ↓
```json  
{
    "user_id": 2,
    "nick_name": "微微笑"
}
user_id 粉丝的id
nick_name 粉丝的昵称
```  

type=3 发贷超通知
```json  
ticker 标题栏信息
title 标题
text 描述
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
description 关键词  
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
		"huanxin_uuid": "",
                "huanxin_nickname": "",
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
		"huanxin_uuid": "",
                "huanxin_nickname": "",
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

### 和我聊聊
- 请求方式: `get`
- 请求地址: {host}`business/set-interest?id=`

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": []
}
```


### 信息
- 请求方式: `get`
- 请求地址: {host}`my-center/get-focus-info?id=1`
- 请求参数:  id  是用户的id

- 响应内容:  
```json
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "focus_num": 4,
        "focused_num": 2,
        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
        "nick_name": "微微笑",
        "focus": 1,
        "mobile": "150****0110",
        "gender": "男",
        "city_name": "北京市东城区"
    }
}
foucus_num关注数，focused_num被关注数,focus 1代表已经关注 ,avatar_image 头像
```




### 发布的文章
- 请求方式: `get`
- 请求地址: {host}`articles?creater=110&page=1&per-page=3`
- 请求参数:  creater是用户的id，后面的参数代表page=1第一页,per-page显示3条

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
- 请求地址: {host}`businesses?u_id=1&page=1&per-page=10`
- 请求参数:  uid,用户id，后面的是分页 第一页 取10条

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

### 我的订阅
- 请求方式: `get`
- 请求地址: {host}`article-type/list?id=1?page=1&per-page=10`
- 请求参数:  id 用户的id， page=1&per-page=10分页参数

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
                "subscription_num": 114,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82107701.jpg",
                "is_del": 0
            },
            {
                "at_id": 14,
                "at_name": "投资指南",
                "topic": "专题6",
                "topic_des": "描述6",
                "subscription_num": 177,
                "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/54815439.jpg",
                "is_del": 0
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/article-type/list?id=1&page=1"
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
topic是标题 topic_des 是副标题 
```


### 通知消息设置
- 请求方式: `get`
- 请求地址: {host}`message-setting/toggle?type=1&status=1`
- 请求参数:  type 1评论或回复 2关注了你， status 传0 设置成任何人，传1 设置成从不提醒

- 响应内容:  
```json
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "id": 4,
        "user_id": 1,
        "comment_reply": 0,
        "focus": 1,
        "praise": 0
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
	"email": "联系人邮箱 也是可选的",
	"pics":["https://www.baidu.com","https://www.jd.com"]
}
```
- 响应内容:  
```json
不需要关注
```




### 编辑个人资料
- 请求方式: `put`
- 请求地址: {host}`user/update`
- 请求参数:  
注： 更新什么就传什么参，光更新手机号就只需要传手机号
```json
{
	"nick_name":"微微笑",
	"mobile": "15061690110",
	"gender": 0,
	"avatar_image" : "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg"
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "更新成功",
    "info": {
        "id": 1,
        "mobile": "15061690110",
        "access_token": "o2iSTUyXyr0ij-1m22KAuToup00JaZ1S",
        "nick_name": "微微笑",
        "wechat_token": "dad",
        "qq_token": "djehwgqwj",
        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
        "register_time": "2019-07-11 14:33:50",
        "last_login_time": "2019-08-20 18:01:11",
        "register_ip": "31.84.183.44"
    }
}
```




### 关注作者
- 请求方式: `post`
- 请求地址: {host}`my-center/focus`
- 请求参数:  
注： id用户的id
```json
{
	"id": 18
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "active": 0
    }
}
1代表点击关注了，  0代表取消了关注
```



### ta的关注和粉丝
- 请求方式: `get`
- 请求地址: {host}`focu/fan-focus?id=1&type=1&page=1&per-page=10`
- 请求参数:  
注： id用户的id  type=1是关注列表 type=2是粉丝列表  page=1&per-page=10分页参数

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "user_id": "172",
                "nick_name": "美妆师A4",
		"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/62621043.jpg",
                "is_focus": "0"
            },
            {
                "user_id": "187",
                "nick_name": "你为何放弃治疗",
		"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/62621043.jpg",
                "is_focus": "1"
            },
            {
                "user_id": "13",
                "nick_name": "怂咖",
                "is_focus": "0"
            },
            {
                "user_id": "167",
                "nick_name": "缠绵过后",
		"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/62621043.jpg",
                "is_focus": "0"
            },
            {
                "user_id": "212",
                "nick_name": "小可爱",
		"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/62621043.jpg",
                "is_focus": "0"
            },
            {
                "user_id": "162",
                "nick_name": "仙人球",
		"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/62621043.jpg",
                "is_focus": "0"
            },
            {
                "user_id": "219",
                "nick_name": "无情",
		"avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/62621043.jpg",
                "is_focus": "0"
            }
        ],
        "_meta": {
            "totalCount": 7,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
type 1和2  返回的数据格式一致
is_focus    1代表已关注，  0代表未关注   不登录的话都是未关注的状态点击关注需要登录
```


## 电台
### 电台列表
- 请求方式: `get`
- 请求地址: {host}`radios?sort=-id&page=1&per-page=20`  
sort=-id 表示最新的时间排在最上面， sort=id 代表最老的时间在最上面   page=1&per-page=20 分页参数
- 响应参数:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 2,
                "type": 1,
                "origin": "来源2",
                "title": "标题2",
                "desc": "描述",
                "preview_image": "https://www.baidu.com",
                "comment_num": 0,
                "like_num": 0,
                "create_time": "2019-09-26",
                "creater": 25,
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/95849225.jpg",
                "author": "凉汜",
                "before_time": "2小时前",
                "like": 0,
                "collect_num": 0,
                "collect": 0
            },
            {
                "id": 1,
                "type": 1,
                "origin": "来源",
                "title": "标题",
                "desc": "描述",
                "preview_image": "https://www.baidu.com",
                "comment_num": 0,
                "like_num": 0,
                "create_time": "2019-09-26",
                "creater": 25,
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/95849225.jpg",
                "author": "凉汜",
                "before_time": "2小时前",
                "like": 0,
                "collect_num": 1,
                "collect": 0
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radios?page=1"
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


### 电台列表详情
- 请求方式: `get`
- 请求地址: {host}`radios/1?expand=content,label,recommend,read_recommend`
- 请求参数:  
1 是电台的id， ? 后面参数写死

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "type": 1,
                "origin": "来源",
                "title": "标题",
                "desc": "描述",
                "preview_image": "https://www.baidu.com",
                "comment_num": 0,
                "like_num": -2,
                "create_time": "2019-09-26",
                "creater": 25,
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/95849225.jpg",
                "author": "凉汜",
                "before_time": "4小时前",
                "like": 0,
                "collect_num": 0,
                "collect": 0,
                "content": "内容",
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
		"recommend": [
                    {
                        "id": "2",
                        "images": "https://www.baidu.com",
                        "title": "标题2",
                        "type": "1",
                        "like_num": "0",
                        "comment_num": "0"
                    }
                ],
		"read_recommend": [
                    {
                        "id": 291,
                        "images": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-08-07/gAGO0BvJl7nGPVyku2U7cnx0XpMVZbSE.jpg",
                        "title": "如何快速在职场崛起",
                        "create_time": "2019-08-07 12:15:57",
                        "desc": "少走弯路，快速成长",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/55400530.jpg",
                        "like_num": 19,
                        "comment_num": 1
                    },
                    {
                        "id": 198,
                        "images": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-08-05/Bk7tSgMyvVfk2sHQ2ycvaSVPWX9aqjha.jpg",
                        "title": "职场升级手册",
                        "create_time": "2019-08-05 13:09:39",
                        "desc": "职场升级必须了解这些",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/90265104.jpg",
                        "like_num": 22,
                        "comment_num": 0
                    },
                    {
                        "id": 714,
                        "images": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-08-30/_czXvNhTt5wNrcK8kCeclVgvUujLsl2x.jpg",
                        "title": "月入一万和月入十万的根本区别在哪里？",
                        "create_time": "2019-08-30 11:45:34",
                        "desc": "行业和职位是决定性因素",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/55883130.jpg",
                        "like_num": 47,
                        "comment_num": 0
                    }
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radios/1?expand=content%2Clabel%2Crecommend&page=1"
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
### 电台点赞
- 请求方式: `post`
- 请求地址: {host}`radio-like/like`
- 请求参数:  

```json
{
	"id":1
}
id 是电台的id
```  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "active": 0
    }
}
active 1 代表点赞成功 切换成了已经点赞的状态
active 0 取消点赞成功
```



### 电台收藏
- 请求方式: `post`
- 请求地址: {host}`radio-collect/collect`
- 请求参数:  

```json
{
	"id":1
}
id 是电台的id
```  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "active": 0
    }
}
active 1 代表收藏成功 切换成了已经收藏了状态
active 0 取消收藏成功
```

### 电台评论个数
- 请求方式: `get`
- 请求地址: {host}`get-count?id=1`
- 请求参数:  id为电台id


id 是电台的id
```  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "count": 2
    }
}
```




### 电台列表内页的评论
- 请求方式: `get`
- 请求地址: {host}`radio-comments?radio_id=1&type=no_child&per-page=3`
- 请求参数:  

id 是电台的id


- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 2,
                "radio_id": 1,
                "user_id": 110,
                "content": "评论了一下文222",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 2,
                "create_time": "2019-09-26 15:03:23",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "阿军666",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-24/Pbz6lnGFMImGC76WNnbtL20lEKv4tLkt.png",
                "time_before": "3小时前",
                "like": 0,
                "like_count": "0"
            },
            {
                "id": 3,
                "radio_id": 1,
                "user_id": 1,
                "content": "评论33",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 1,
                "create_time": "2019-09-26 15:09:21",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "3小时前",
                "like": 1,
                "like_count": "1"
            },
            {
                "id": 1,
                "radio_id": 1,
                "user_id": 1,
                "content": "评论内容11",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 1,
                "create_time": "2019-09-26 14:48:16",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "3小时前",
                "like": 0,
                "like_count": "0"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radio-comments?radio_id=1&type=no_child&per-page=3&page=1"
            }
        },
        "_meta": {
            "totalCount": 3,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 3
        }
    }
}
```






### 电台最新评论
- 请求方式: `get`
- 请求地址: {host}`radio-comments?radio_id=1&type=new&pid=0&page=1&per-page=20`
- 请求参数:  

id 是电台的id  page=1&per-page=20分页参数 自行设定，不传也可


- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 3,
                "radio_id": 1,
                "user_id": 1,
                "content": "评论33",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 1,
                "create_time": "2019-09-26 15:09:21",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "3小时前",
                "like": 1,
                "like_count": "1",
                "child": []
            },
            {
                "id": 2,
                "radio_id": 1,
                "user_id": 110,
                "content": "评论了一下文222",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 2,
                "create_time": "2019-09-26 15:03:23",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "阿军666",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-24/Pbz6lnGFMImGC76WNnbtL20lEKv4tLkt.png",
                "time_before": "3小时前",
                "like": 0,
                "like_count": "0",
                "child": [
                    {
                        "id": 4,
                        "radio_id": 1,
                        "user_id": 13,
                        "content": "我回复了",
                        "pid": 2,
                        "reply_pid": 2,
                        "like_num": 0,
                        "child_count": 0,
                        "create_time": "2019-09-26 16:10:15",
                        "update_time": null,
                        "del": 0,
                        "is_private": 0,
                        "time_before": "2小时前",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82888066.jpg",
                        "nick_name": "怂咖",
                        "like": 0,
                        "like_count": 0,
                        "replied_user_id": 110,
                        "replied_nick_name": "阿军666"
                    }
                ]
            },
            {
                "id": 1,
                "radio_id": 1,
                "user_id": 1,
                "content": "评论内容11",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 1,
                "create_time": "2019-09-26 14:48:16",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "3小时前",
                "like": 0,
                "like_count": "0",
                "child": []
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radio-comments?radio_id=1&type=new&page=1"
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




### 电台最热评论
- 请求方式: `get`
- 请求地址: {host}`radio-comments?radio_id=1&type=hot&pid=0&page=1&per-page=20`
- 请求参数:  

id 是电台的id  page=1&per-page=20分页参数 自行设定，不传也可
数据格式与最新评论是一致的 


- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 2,
                "radio_id": 1,
                "user_id": 110,
                "content": "评论了一下文222",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 2,
                "create_time": "2019-09-26 15:03:23",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "阿军666",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-24/Pbz6lnGFMImGC76WNnbtL20lEKv4tLkt.png",
                "time_before": "3小时前",
                "like": 0,
                "like_count": "0",
                "child": [
                    {
                        "id": 4,
                        "radio_id": 1,
                        "user_id": 13,
                        "content": "我回复了",
                        "pid": 2,
                        "reply_pid": 2,
                        "like_num": 0,
                        "child_count": 0,
                        "create_time": "2019-09-26 16:10:15",
                        "update_time": null,
                        "del": 0,
                        "is_private": 0,
                        "time_before": "2小时前",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82888066.jpg",
                        "nick_name": "怂咖",
                        "like": 0,
                        "like_count": 0,
                        "replied_user_id": 110,
                        "replied_nick_name": "阿军666"
                    }
                ]
            },
            {
                "id": 3,
                "radio_id": 1,
                "user_id": 1,
                "content": "评论33",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 1,
                "create_time": "2019-09-26 15:09:21",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "3小时前",
                "like": 1,
                "like_count": "1",
                "child": []
            },
            {
                "id": 1,
                "radio_id": 1,
                "user_id": 1,
                "content": "评论内容11",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 1,
                "create_time": "2019-09-26 14:48:16",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "3小时前",
                "like": 0,
                "like_count": "0",
                "child": []
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radio-comments?radio_id=1&type=hot&page=1"
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





### 电台评论详情
- 请求方式: `get`
- 请求地址: {host}`radio-comments/2`
- 请求参数:  
/2  是评论的id

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 2,
                "radio_id": 1,
                "user_id": 110,
                "content": "评论了一下文222",
                "pid": 0,
                "reply_pid": 0,
                "like_num": 0,
                "child_count": 2,
                "create_time": "2019-09-26 15:03:23",
                "update_time": null,
                "del": 0,
                "is_private": 0,
                "comment_count": "4",
                "nick_name": "阿军666",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-24/Pbz6lnGFMImGC76WNnbtL20lEKv4tLkt.png",
                "time_before": "19小时前",
                "like": 0,
                "like_count": "0",
                "child": [
                    {
                        "id": 4,
                        "radio_id": 1,
                        "user_id": 13,
                        "content": "我回复了",
                        "pid": 2,
                        "reply_pid": 2,
                        "like_num": 0,
                        "child_count": 0,
                        "create_time": "2019-09-26 16:10:15",
                        "update_time": null,
                        "del": 0,
                        "is_private": 0,
                        "time_before": "18小时前",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82888066.jpg",
                        "nick_name": "怂咖",
                        "like": 0,
                        "like_count": 0,
                        "replied_user_id": 110,
                        "replied_nick_name": "阿军666"
                    }
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radio-comments/2?page=1"
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




### 电台post评论
- 请求方式: `post`
- 请求地址: {host}`radio-comments`
- 请求参数:  

```json
{
	"id": 2,
	"content":"评论电台",
	"pid": 0
}
id radio的id，pid 0 是代表评论电台，其他则是回复评论。
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "添加成功",
    "info": {
        "id": 9,
        "radio_id": 2,
        "content": "哈哈哈",
        "create_time": "2019-09-27 17:41:00",
        "user_id": 1,
        "pid": 0,
        "reply_pid": 0,
        "is_private": 0,
        "del": 0,
        "nick_name": "微微笑",
        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
        "time_before": "刚刚"
    }
}
```


### 电台举报
- 请求方式: `post`
- 请求地址: {host}`radio-reports`
- 请求参数:  

```json
{
	"id":1,
	"content":"举报内容"
}
id radio的id
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "操作成功",
    "info": ""
}
```



### 电台评论点赞
- 请求方式: `put`
- 请求地址: {host}`radio-comment-likes/2`
- 请求参数:  

```json

```

- 响应内容:  

```json
{
    "code": 1,
    "message": "添加成功",
    "info": {
        "active": 1
    }
}
1 已点赞
```




### 电台时间轴
- 请求方式: `get`
- 请求地址: {host}`radio-shafts?id=1`
- 请求参数:   id 是电台的id


- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "radio_id": 1,
                "at": 0,
                "title": "开场白",
		"image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82888066.jpg",
                "content": "我是开车白",
                "quote_href": "https://www.baidu.com"
            },
            {
                "id": 2,
                "radio_id": 1,
                "at": 10,
                "title": "标题",
		"image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82888066.jpg",
                "content": "内容",
                "quote_href": ""
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radio-shafts?id=1&page=1"
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
content是内容，quote_href是外链，可能有外链，表示引用了别人的  at时间点，0代表第0秒的时刻
```

### 电台banner
- 请求方式: `get`
- 请求地址: {host}`radio/new`
- 请求参数: 

```json

```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 4,
        "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-10-15/0ic789-zUCHJQw6av6cuXvbb0kr1XPTS.jpg"
    }
}
```




### 我的电台
- 请求方式: `get`
- 请求地址: {host}`radios?my=1`
- 请求参数:  全部写死

```json

```
- 响应内容:   参考电台列表
```json

```





### 电台标题搜索
- 请求方式: `get`
- 请求地址: {host}`radios?title=%要搜索的内容%`
- 请求参数: 直接把要搜索的内容传递到参数上

```json

```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 7,
                "radio_url": "http://xijin-test.oss-cn-shanghai.aliyuncs.com/radio/2019-10-15/1571132739853.mp3",
                "size": "88393.52",
                "type": 0,
                "origin": "",
                "title": "低成本创业是不是一个伪命题？",
                "desc": "孤注一掷的勇气究竟能否开花结果",
                "preview_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-10-18/xNL52KR6FJCKxzw4JjyMkXtE75a66J0L.png",
                "comment_num": 0,
                "like_num": 25,
                "create_time": "2019-10-15",
                "before_time": "5天前",
                "like": 0,
                "collect_num": 0,
                "collect": 0,
                "share_url": "http://my_xijin_api.com/?id=7&radio_url=http://xijin-test.oss-cn-shanghai.aliyuncs.com/radio/2019-10-15/1571132739853.mp3",
                "radio_time": "36:58",
                "radio_size": "86.32MB",
                "participants": [
                    {
                        "id": 121,
                        "nick_name": "主页菌",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-27/Am7n0XLBqZ_Pffl1JJhgHzf9mCltG_79.png"
                    },
                    {
                        "id": 227,
                        "nick_name": "Ծ‸Ծ",
                        "avatar_image": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTLRbCnyAoRJV6QbTeOicKR3icGsNIxgfkqu6b9Zf4a7ViaVECzzianqFcqPxTRyzLVynlkgRdueibZO7nQ/132"
                    },
                    {
                        "id": 374,
                        "nick_name": null,
                        "avatar_image": null
                    }
                ],
                "radio_shaft": [
                    {
                        "id": 204,
                        "radio_id": 7,
                        "at": 38,
                        "title": "本期内容",
                        "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/article/images/2019-10-18/UrqvpKCnfpdA7vzKMJSCC-Rg77bY7oyf.png",
                        "content": "低成本创业有多难，本期节目我们跟大家聊一聊这个话题。很多时候不一定是创业思路不对，只是在最艰难的时候，没有资金会让你力不从心。",
                        "quote_href": ""
                    }
                  
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/radios?title=%E4%BD%8E%E6%88%90%E6%9C%AC&page=1"
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



## 赚钱圈
### 领域列表
- 请求方式: `get`
- 请求地址: {host}`make-money-types`  
- 响应参数:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": 1,
            "name": "宠物"
        },
        {
            "id": 2,
            "name": "创业"
        },
        {
            "id": 3,
            "name": "奶茶"
        }
    ]
}
```

### 圈子创建
- 请求方式: `post`
- 请求地址: {host}`make-money-groups`
- 请求参数:  

```json
{
	"type_id": "领域列表id",
	"name":"名称",
	"logo": "http://123.456.org",
	"im_group_id": "群组id",
	"description": "描述",
	"announcement": "公告"
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "type_id": "1",
        "name": "名称",
        "logo": "http://123.456.org",
        "im_group_id": "123321",
        "announcement": "",
        "u_id": 1,
        "id": 6
    }
}
```

### 圈子修改
- 请求方式: `put`
- 请求地址: {host}`make-money-groups/:im_group_id`
- 请求参数:  

```json
{
	"type_id": "领域列表id",
	"name":"名称",
	"logo": "http://123.456.org",
	"nums": "人数",
	"announcement": "公告",
	"join_need_consent": "加入是否需要审核 0:不需要，1:需要"
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": "46",
        "u_id": "375",
        "type_id": "1",
        "name": "第一个圈子",
        "logo": "/storage/emulated/0/Android/data/com.xiyi.rhinobillion/cache/luban_disk_cache/1573440058945274.jpeg",
        "nums": "0",
        "announcement": "",
        "im_group_id": "98609944133633",
        "create_time": "2019-11-11 10:42:52",
        "update_time": "2019-11-11 10:42:52",
        "join_need_consent": "0",
        "status": "1",
        "is_owner": 0
    }
}
```

### 圈子信息
- 请求方式: `get`
- 请求地址: {host}`make-money-groups/:im_group_id`
- 请求参数:  
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": "36",
        "u_id": "254",
        "type_id": "3",
        "name": "开奶茶店群1",
        "logo": "https://xijin-test.oss-cn-shanghai.aliyuncs.com/image/1573709508937301.jpeg",
        "nums": "9",
        "upvote_nums": "6",
        "description": "1111111111111",
        "announcement": "1111111111111",
        "im_group_id": "98892384370689",
        "create_time": "2019-11-14 13:32:07",
        "update_time": "2019-11-19 18:53:26",
        "join_need_consent": "0",
        "status": "1",
        "is_owner": 0
    }
}
```

### 圈子删除
- 请求方式: `delete`
- 请求地址: {host}`make-money-groups/:im_group_id`
- 请求参数:  
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": ""
}
```


### 圈子列表
- 请求方式: `get`
- 请求地址: {host}`make-money-groups?type_id=&rand=`
- 请求参数:  rand=1为随机  
- 响应内容:  
join_need_consent  加入需要审核 0: 不需要 1:需要;  
is_new  是否新群 0：否 1： 是  
join_status  进群状态  0:未进群，1：已进群，2：申请中

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 32,
                "u_id": 253,
                "type_id": 5,
                "name": "水果",
                "logo": "https://xijin-test.oss-cn-shanghai.aliyuncs.com/image/1573616440601456.png",
                "nums": 1,
                "upvote_nums": 0,
                "description": "我要吃水果",
                "announcement": "我要吃水果",
                "im_group_id": "98794786062337",
                "create_time": "2019-10-13 11:40:51",
                "update_time": "2019-11-13 14:48:35",
                "join_need_consent": 0,
                "status": 1,
                "is_new": 0,
                "join_status": 1
            },
            {
                "id": 31,
                "u_id": 377,
                "type_id": 2,
                "name": "测试",
                "logo": "https://xijin-test.oss-cn-shanghai.aliyuncs.com/image/157361263285718.jpeg",
                "nums": 1,
                "upvote_nums": 0,
                "description": "",
                "announcement": "",
                "im_group_id": "98790786793476",
                "create_time": "2019-11-13 10:37:17",
                "update_time": "2019-11-13 10:37:17",
                "join_need_consent": 0,
                "status": 1,
                "is_new": 1,
                "join_status": 0
            },
            {
                "id": 30,
                "u_id": 377,
                "type_id": 7,
                "name": "共享资本",
                "logo": "https://xijin-test.oss-cn-shanghai.aliyuncs.com/image/1573545050343395.jpeg",
                "nums": 1,
                "upvote_nums": 0,
                "description": "",
                "announcement": "",
                "im_group_id": "98719919833089",
                "create_time": "2019-11-12 15:50:52",
                "update_time": "2019-11-12 15:50:52",
                "join_need_consent": 0,
                "status": 1,
                "is_new": 1,
                "join_status": 0
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/make-money-groups?per-page=3&page=1"
            },
            "next": {
                "href": "http://xj.org/make-money-groups?per-page=3&page=2"
            },
            "last": {
                "href": "http://xj.org/make-money-groups?per-page=3&page=11"
            }
        },
        "_meta": {
            "totalCount": 31,
            "pageCount": 11,
            "currentPage": 1,
            "perPage": 3
        }
    }
}
```


### 聊天点赞
- 请求方式: `post`
- 请求地址: {host}`im-message-upvote/create`
- 请求参数:  

```json
{
	"group_id": "第三方群组id",
	"message_id":"第三方信息id",
	"upvote_user_id": "当前登录用户第三方用户id"
}
```

- 响应内容:  

```json
{
    "code": 0,
    "message": "existed",
    "info": ""
}
```


### 聊天点赞查询
- 请求方式: `get`
- 请求地址: {host}`im-message-upvote/view?group_id=&upvote_user_id=&message_id=`
- 请求参数:  group_id,upvote_user_id,message_id   注：message_id 可传多个 ',' 拼接  e.g. 1,2,3,4,5

- 响应内容:  
upvote_count： 点赞数  
is_upvoted： 是否已点赞

```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "message_id": "1",
            "upvote_count": 1,
            "is_upvoted": false
        },
        {
            "message_id": "2",
            "upvote_count": 1,
            "is_upvoted": false
        }
    ]
}
```


### 根据第三方用户id查询用户信息
- 请求方式: `get`
- 请求地址: {host}`make-money-group/get-user-info?im_user_id=`
- 请求参数:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 181,
        "mobile": "18888888181",
        "password": null,
        "access_token": "181",
        "nick_name": "微微笑",
        "gender": 1,
        "city_id": null,
        "wechat_token": null,
        "qq_token": null,
        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/16791610.jpg",
        "register_time": "2019-08-01 15:03:27",
        "last_login_time": null,
        "register_ip": null,
        "last_login_ip": null,
        "status": 1,
        "device_id": null,
        "os": null,
        "focus_num": 44,
        "focused_num": 44,
        "login_time": null,
        "active": null,
        "active_time": null,
        "conceal_hide": null,
        "cause_of_violation": "",
        "huanxin_uuid": "d6a16400-d3a0-11e9-bbdf-6321e961491c",
        "huanxin_type": "user",
        "huanxin_created": 2147483647,
        "huanxin_modified": 2147483647,
        "huanxin_username": "18888888181",
        "huanxin_password": "181",
        "huanxin_activated": 1,
        "huanxin_nickname": "18888888181"
    }
}
```

### 圈子成员新增
- 请求方式: `post`
- 请求地址: {host}`make-money-group-users`
- 请求参数:  
u_id 可传多个','拼接  e.g. 1,2,3  
im_u_id 可传多个','拼接  e.g. 1,2,3  
u_id im_u_id 二选一  

```json
{
	"u_id": "用户id",
	"im_group_id": "群组id",
	"im_u_id": "第三方用户id"
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "im_group_id": "1",
        "u_id": "2",
        "im_u_id": "8129f730-d3a0-11e9-8561-d7ace6d28bae",
        "id": 5
    }
}
```

### 圈子成员删除
- 请求方式: `delete`
- 请求地址: {host}`make-money-group-user/delete?u_id=&im_group_id=&im_u_id=`
- 请求参数:  
u_id 可传多个','拼接  e.g. 1,2,3  
im_u_id 可传多个','拼接  e.g. 1,2,3  
u_id im_u_id 二选一  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": ""
}
```

### 圈子成员列表
- 请求方式: `delete`
- 请求地址: {host}`make-money-group-users?im_group_id=`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 2,
                "u_id": 2,
                "im_u_id": "8129f730-d3a0-11e9-8561-d7ace6d28bae",
                "im_group_id": "1",
                "create_time": "2019-11-13 14:00:31",
                "nick_name": "陌南尘",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/50939351.jpg"
            },
            {
                "id": 5,
                "u_id": 2,
                "im_u_id": "8129f730-d3a0-11e9-8561-d7ace6d28bae",
                "im_group_id": "1",
                "create_time": "2019-11-13 14:33:00",
                "nick_name": "陌南尘",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/50939351.jpg"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/make-money-group-users?im_group_id=1&page=1"
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

### 用户信息查询
- 请求方式: `post`
- 请求地址: {host}`make-money-group-user/users`

- 请求参数:  

```json
{
    "im_u_id":[
        "15755168442",
        "15901725624",
        "18308461696"
    ]
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 2,
                "nick_name": "陌南尘",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/50939351.jpg",
                "huanxin_uuid": "8129f730-d3a0-11e9-8561-d7ace6d28bae"
            },
            {
                "id": 7,
                "nick_name": "青莳",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/82107701.jpg",
                "huanxin_uuid": "821da600-d3a0-11e9-a4a3-fdc526cebe1b"
            },
            {
                "id": 9,
                "nick_name": "落幕",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/13706446.jpg",
                "huanxin_uuid": "827cb5f0-d3a0-11e9-84ec-07ac2d1f5769"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/make-money-group-user/users?page=1&per-page=200"
            }
        },
        "_meta": {
            "totalCount": 3,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 200
        }
    }
}
```

### 关注用户列表
- 请求方式: `get`
- 请求地址: {host}`focu/my-focus`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "user_id": "1",
            "nick_name": "微微笑",
            "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
            "huanxin_username": "15061690111"
        },
        {
            "user_id": "220",
            "nick_name": "天马行空",
            "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/29491511.jpg",
            "huanxin_username": "18888888220"
        },
        {
            "user_id": "125",
            "nick_name": "微笑",
            "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/16479535.jpg",
            "huanxin_username": "18888888125"
        }
    ]
}
```

### 名片背景图列表
- 请求方式: `get`
- 请求地址: {host}`business-card-backgrounds`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "img_url": "1",
                "sort_num": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/business-card-backgrounds?page=1&per-page=888"
            }
        },
        "_meta": {
            "totalCount": 1,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 888
        }
    }
}
```

### 名片列表
- 请求方式: `get`
- 请求地址: {host}`business-cards`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 3,
                "u_id": 110,
                "name": "1",
                "position": "2",
                "mobile": "3",
                "wechat_username": "4",
                "b_id": 1,
                "background_img": "http://123.456.org"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/business-cards?page=1&per-page=888"
            }
        },
        "_meta": {
            "totalCount": 1,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 888
        }
    }
}
```

### 名片新增
- 请求方式: `post`
- 请求地址: {host}`business-cards`
- 请求参数:  
name 姓名  
position 职位  
mobile 手机号  
wechat_username 微信用户名  
b_id 背景图id  
company_name 公司名  

- 响应内容:  

```json
{
    "code": 1,
    "message": "创建成功",
    "info": {
        "name": "1",
        "position": "2",
        "mobile": "3",
        "wechat_username": "4",
        "u_id": 110,
        "id": 3
    }
}
```

### 名片修改
- 请求方式: `put`
- 请求地址: {host}`business-cards/:id`
- 请求参数:  
name 姓名  
company_name 公司名  
position 职位  
mobile 手机号  
wechat_username 微信用户名  
b_id 背景图id  
company_name 公司名  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 1,
        "u_id": 1,
        "name": "1",
        "position": "2",
        "mobile": "3",
        "wechat_username": "4"
    }
}
```

### 名片删除
- 请求方式: `delete`
- 请求地址: {host}`business-cards/:id`
- 请求参数:  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": ""
}
```

### 更改群主
- 请求方式: `post`
- 请求地址: {host}`make-money-group/change-owener`
- 请求参数:  
im_group_id   
im_u_id   

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 62,
        "u_id": "3",
        "type_id": 16,
        "name": "家居",
        "logo": "https://xijin-test.oss-cn-shanghai.aliyuncs.com/image/1574304338497.jpg",
        "nums": 4,
        "upvote_nums": 2,
        "description": "落后",
        "announcement": "候哦",
        "im_group_id": "99363093282817",
        "create_time": "2019-11-19 18:13:51",
        "update_time": "2019-11-21 11:42:16",
        "join_need_consent": 0,
        "status": 0,
        "is_new": 1,
        "join_status": 0
    }
}
```

### 小报当日数量统计
- 请求方式: `get`
- 请求地址: {host}`week-news/list?type=count`
- 请求参数:  

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": {
        "count": 3
    }
}
```

### 小报列表
- 请求方式: `get`
- 请求地址: {host}`week-news/list?type=list`
- 请求参数:  page

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": {
        "date": "12-09",
        "count": 3,
        "items": [
            {
                "id": "9",
                "title": "ofo再出退押金新招：想退99元，先消费1500元",
                "content": "近日，ofo推出了一个退押金新招：在App首页上线了“天天返钱”的活动，告知用户“无需排队，直接退还押金”。参加活动的用户，其押金会转至“天天返钱”账户，用户必须在ofo商城里通过额外消费后才有返现，押金会以双倍返现的形式退还给用户。换句话说，用户至少需要购物1500元，才可提现120多元，相当于“拿回”99元押金。这与此前押金换金币的玩法相似。"
            },
            {
                "id": "7",
                "title": "拼多多孵化直播业务：内测微信小程序对标淘宝直播",
                "content": "从多个信源处获悉，拼多多正在孵化直播业务，于11月24日前后首先内测微信小程序。一位接近拼多多的人士称，拼多多联合创始人达达（孙沁）亲自盯项目，并负责具体的业务沟通，也是直播业务的最高负责人。此外一些招聘网站已有相关信息流出。拉勾网显示，拼多多正在招聘“网红机构运营经理”、“视频创意经理”等与直播相关的职位。"
            },
            {
                "id": "8",
                "title": "BOSS直聘完成数亿美元融资，领投方包括腾讯",
                "content": "BOSS直聘已于近期完成新一轮融资，融资总规模达到数亿美金。一位接近交易的知情人士透露，这轮融资“分多次，有E1和E2”，腾讯参与并领投了其中一轮，投后占股接近10%，BOSS直聘会把融到的钱继续花在流量和用户增长上。对此，BOSS直聘方表示不予回应，腾讯公关“不予置评”。"
            }
        ],
        "_meta": {
            "totalCount": 3,
            "pageCount": 3,
            "currentPage": "1",
            "perPage": 1
        }
    }
}
```

### 赚钱圈banner
- 请求方式: `get`
- 请求地址: {host}`make-money-banners`
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
                "type": 0,
                "pic": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-12-09/%E7%BC%96%E7%BB%84%2029%402x.png"
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.org/make-money-banners?page=1"
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

### 赚钱圈圈子信息
- 请求方式: `get`
- 请求地址: {host}`make-money-group/list?im_group_id=`
- 请求参数:  im_group_id 多个',' 拼接 e.g. 1,2,3,4,5

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "im_group_id": "99993166872577",
            "type_id": "2",
            "type_name": "创业"
        },
        {
            "im_group_id": "100021273952257",
            "type_id": "3",
            "type_name": "奶茶"
        },
        {
            "im_group_id": "100032309166081",
            "type_id": "3",
            "type_name": "奶茶"
        }
    ]
}
```

### 个人中心我/他的圈子
- 请求方式: `get`
- 请求地址: {host}`make-money-group/center-list?u_id=&per-page=`
- 请求参数:  u_id不传时表示个人中心

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "7",
            "name": "测试群数据",
            "im_group_id": "100514439168001",
            "logo": "https://xijin-test.oss-cn-shanghai.aliyuncs.com/image/1574934276199.jpg",
            "type_id": "16",
            "type_pic": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-12-17/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20191218111231.png"
        }
    ]
}
```
