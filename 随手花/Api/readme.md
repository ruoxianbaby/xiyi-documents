## **用户端api**
<a href="./#用户端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [user模块](./#user模块)  
    - [获取短信验证码](./#获取短信验证码)  
    - [获取access_token](./#获取access_token)
    - [获取用户信息接口](./#获取用户信息)  
    - [获取用户申请记录](./#获取用户申请记录)
- [产品模块](./#产品模块)  
    - [申请贷款接口](./#申请贷款接口)
    - [获取首页精品](./#获取首页精品)
    - [获取首页热门推荐产品](./#获取首页热门推荐产品-同获取推荐贷款)  
    - [获取首页最新口子](./#获取首页最新口子)  
    - [获取贷款大全首次加载](./#获取贷款大全首次加载)  
    - [获取贷款详情](./#获取贷款详情)  
    - ~~[获取必下款](./#获取必下款)~~
    - ~~[获取推荐贷款](./#获取首页热门推荐产品-同获取推荐贷款) **同获取首页产品**~~  
- [其他](./#其他)  
    - [刷单](./#刷单)  
    - [用户反馈](./#用户反馈)  
    - [商务合作](./#商务合作)  
    - [获取审核接口](./#获取审核接口)  
    - [上报设备号](./#上报设备号)  
    - [渠道推广页](./#渠道推广页)  
        - [获取csrf](./#获取csrf)  
	- [获得渠道id](./#获得渠道id)
   - [获取产品url](./#获取产品url)
- [论坛](./#论坛)  
    - [栏目](./#栏目)   
    - [文章](./#文章)

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
- 请求参数: `access_token=4W1ZD1h_94Jmrx5PKqA24M-iuYvG8ce8`

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
### 获取用户申请记录

## 产品模块  
### 申请贷款接口  
- 请求方式: `post`
- 请求地址: {host}`apply`
- 请求参数: 
```json
{
	"user_id": 10,
	"product_id": 10
}
```  
- 响应内容: 
```json
{
    "code": 1,
    "message": "success",
    "info": []
}
```

### 获取首页精品  
- 请求方式: `get`
- 请求地址: {host}`products?per-page=1&sort=sort`
- 请求参数: `per-page=1&sort=sort`  
- 说明:  
>fields: 只显示给定的字段,多字段用`,`号隔开  
>per-page: 每页数量  
>page: 第几页  
>sort: 根据那个字段排序,多字段用`,`号隔开, 逆序字段名前加`-`号  
- 响应内容:  
```json
    {
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 13,
                "name": "24随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "slogan": null,
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 0,
                "status": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8081/products?type=hot&per-page=1&page=1"
            },
            "next": {
                "href": "http://localhost:8081/products?type=hot&per-page=1&page=2"
            },
            "last": {
                "href": "http://localhost:8081/products?type=hot&per-page=1&page=5"
            }
        },
        "_meta": {
            "totalCount": 5,
            "pageCount": 5,
            "currentPage": 1,
            "perPage": 1
        }
    }
}
```

### 获取首页热门推荐产品 **同获取推荐贷款**
- 请求方式: `get`
- 请求地址: {host}`products?type=1&per-page=10`
- 请求参数: `type=1&per-page=10`  
 
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 8,
                "name": "给个手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 7,
                "name": "dDA手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 9,
                "name": "发送随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 6,
                "name": "kk随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 12,
                "name": "25随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 11,
                "name": "约了随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 10,
                "name": "台湾随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 13,
                "name": "24随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 4,
                "name": "随手花2gdsg",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 5,
                "name": "rqwer手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8081/products?type=1&per-page=10&page=1"
            },
            "next": {
                "href": "http://localhost:8081/products?type=1&per-page=10&page=2"
            },
            "last": {
                "href": "http://localhost:8081/products?type=1&per-page=10&page=2"
            }
        },
        "_meta": {
            "totalCount": 13,
            "pageCount": 2,
            "currentPage": 1,
            "perPage": 10
        }
    }
}
```

### 获取首页最新口子
- 请求方式: `get`
- 请求地址: {host}`products?type=new&per-page=4`
- 请求参数: `type=new&per-page=4`    

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 3,
                "name": "随dad花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 9,
                "name": "发送随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 7,
                "name": "dDA手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 10,
                "name": "台湾随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8081/products?type=1&per-page=4&page=1"
            },
            "next": {
                "href": "http://localhost:8081/products?type=1&per-page=4&page=2"
            },
            "last": {
                "href": "http://localhost:8081/products?type=1&per-page=4&page=4"
            }
        },
        "_meta": {
            "totalCount": 13,
            "pageCount": 4,
            "currentPage": 1,
            "perPage": 4
        }
    }
}
```

### 获取贷款详情 
- 请求方式: `get`  
- 请求地址: {host}`products/:id`  
- 请求参数: `:id`  
- 响应内容:
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 1,
        "name": "随手花",
        "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
        "slogan": null,
        "desc": "3分钟下款",
        "max_price": 50000,
        "apply_price": "2000-50000",
        "rate": "0.3%",
        "apply_num": 25456,
        "lending_time": 3,
        "max_duration": 14,
        "apply_duration": null,
        "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
        "hot": 1,
        "pass": 1,
        "sort": 10,
        "status": 1
    }
}
```  
### 获取贷款大全首次加载
- 请求方式: `get`
- 请求地址: {host}`products?per-page=10&page=1&sort=sort`
- 请求参数: `per-page=10&page=1&sort=sort`  

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 13,
                "name": "24随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 0,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 12,
                "name": "25随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 1,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 11,
                "name": "约了随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 2,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 1,
                "name": "随手花",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 10,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 2,
                "name": "随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 11,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 4,
                "name": "随手花2gdsg",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 11,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 7,
                "name": "dDA手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 11,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 8,
                "name": "给个手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 12,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 9,
                "name": "发送随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 13,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 10,
                "name": "台湾随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 0,
                "sort": 14,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8081/products?per-page=10&page=1&sort=sort"
            },
            "next": {
                "href": "http://localhost:8081/products?per-page=10&page=2&sort=sort"
            },
            "last": {
                "href": "http://localhost:8081/products?per-page=10&page=2&sort=sort"
            }
        },
        "_meta": {
            "totalCount": 13,
            "pageCount": 2,
            "currentPage": 1,
            "perPage": 10
        }
    }
}
```
### 获取必下款
- 请求方式: `get`
- 请求地址: {host}`products?type=2&per-page=10&sort=sort`
- 请求参数: `type=2&per-page=10&sort=sort`  

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "name": "随手花",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 10,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 2,
                "name": "随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 11,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 4,
                "name": "随手花2gdsg",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 11,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 3,
                "name": "随dad花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Upload",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "hot": 1,
                "pass": 1,
                "sort": 20,
                "money": "500000",
                "status": 1,
                "user_price": 20,
                "platform": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8081/products?sort=sort&type=2per-page%3D10&page=1"
            }
        },
        "_meta": {
            "totalCount": 4,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```

## 其他
### 刷单  
- 请求方式: `post`
- 请求地址: {host}`click-farm`
- 请求参数:   
```json
{
    "mobile": 15061690110
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

### 用户反馈  
- 请求方式: `post`
- 请求地址: {host}`feedback`
- 请求参数:   
```json
{
    "type": 1,
    "user_id": 10,
    "feedback_type": 1,
    "content": "你的🐎死了"
}
```  

- 响应内容:  
```json
{
    "code": 1,
    "message": "提交成功",
    "info": ""
}	
```  
### 商务合作  
- 请求方式: `post`
- 请求地址: {host}`feedback`
- 请求参数:   
```json
{
    "type": 2,
    "content": "你的🐎死了",
    "user_name": "zzz",
    "email": "123@qq.com"
}
```  

- 响应内容:  
```json
{
    "code": 1,
    "message": "提交成功",
    "info": ""
}	
``` 
### 获取审核接口
- 请求方式: `get`
- 请求地址: {host}`init_app?os=1&channel=baidu&version=1`
- 请求参数: `os=1&channel=baidu&version=1`   
> 说明: 通过auditing字段判断1审核显示论坛, 0则反之. os字段,系统1android,2ios,3web,4其他. 需要判断items是否为[].
- 响应内容:  
```json
{
    "items": [
        {
            "id": 1,
            "name": "first",
            "os": 1,
            "channel": "baidu",
            "status": 1,
            "auditing": 1,
            "version": "1"
        }
    ],
    "_links": {
        "self": {
            "href": "http://localhost:8081/auditing?os=1&channel=baidu&page=1"
        }
    },
    "_meta": {
        "totalCount": 1,
        "pageCount": 1,
        "currentPage": 1,
        "perPage": 20
    }
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

### 渠道推广页  
#### 获取csrf  
- 请求方式: `get`
- 请求地址: `{host}csrf`
- 响应内容:  
```json
{
    "code": 1,
    "message": "Br0VaEKwNOj2ArTQbsT46PC1FMhBFGcYDkwT3iIGmOFV62w-cN9lkaRQ9oND8M2ktMVxkABWEHBkPSunZlze1w==",
    "info": ""
}
```

#### 获得渠道id  
- 请求方式: `post`
- 请求地址: `{host}spread/get-channel-id`  
- 请求参数: 
`
_csrf-api:ha5IRNHe3xPnMMLqICzj31uLpp4R7Gqg6I0pXBEeiQDW-DES47GOarVigLkNGNaTH_vDxlCuHciC_BElVUTPNg==
channel_sign:dAcU9w-zfxDEdnj9rQAmk9_k9jUcWUHZ
` 

- 响应内容:  
```json
{
    "code": 1,
    "message": 8,
    "info": ""
}
```
### 获取产品url
- 请求方式: `get`
- 请求地址: `{host}product-url?prod_sign=12`
- 响应内容:  
```json
{
    "code": 1,
    "message": "Br0VaEKwNOj2ArTQbsT46PC1FMhBFGcYDkwT3iIGmOFV62w-cN9lkaRQ9oND8M2ktMVxkABWEHBkPSunZlze1w==",
    "info": ""
}
```

## 论坛  
### 栏目  
- 请求方式: `get`
- 请求地址: `http://47.103.61.179:83/index.php?r=site%2Fcolumn`
- 响应内容:  
```json
{"status":1,"message":"success","info":[{"id":1,"name":"金融","status":1,"sort":1},{"id":2,"name":"推荐","status":1,"sort":1},{"id":3,"name":"科技","status":1,"sort":1},{"id":4,"name":"创业","status":1,"sort":1},{"id":5,"name":"内幕","status":1,"sort":1}]}
```
### 文章  
- 请求方式: `get`
- 请求地址: `http://47.103.61.179:83/index.php?r=site%2Farticle`
- 响应内容:  

