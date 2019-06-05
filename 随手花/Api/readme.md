# 用户端api

- [user模块](./#user模块)  
    - [获取短信验证码](./#获取短信验证码)  
    - [获取access_token](./#获取access_token)
    - [获取用户信息接口](./#获取用户信息)  
    - [获取用户申请记录](./#获取用户申请记录)
- [产品模块](./产品模块)  
    - [获取首页产品](./#获取首页产品)  
    - [获取首页4个产品](./#获取首页4个产品)  
    - [获取贷款大全首次加载](./#获取贷款大全首次加载)  
    - [获取必下款](./#获取必下款)  
    - [获取推荐贷款](./#获取推荐贷款)

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
- 请求地址: {host}`users/0?access_token=4W1ZD1h_94Jmrx5PKqA24M-iuYvG8ce8`
- 请求参数:  

```
access_token=4W1ZD1h_94Jmrx5PKqA24M-iuYvG8ce8
```  
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
### 获取首页产品
- 请求方式: `get`
- 请求地址: {host}`products?type=1&per-page=10`
- 请求参数:  
```type=1&per-page=10```  
- 说明: ```
per-page: 每页数量
page: 第几页
sort: 根据那个字段排序,多字段用`,`号隔开, 逆序字段名前加`-`
```
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

### 获取首页4个产品
- 请求方式: `get`
- 请求地址: {host}`products?type=1&per-page=4`
- 请求参数:  
```type=1&per-page=4```  

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
### 获取贷款大全首次加载
- 请求方式: `get`
- 请求地址: {host}`products?per-page=10&page=1&sort=sort`
- 请求参数:  
```per-page=10&page=1&sort=sort```  

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
