## **服务端api**
<a href="./#服务端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [Admin模块](./#用户模块)  
    - [获取access_token](./#获取access_token)  
    - [access_token换取用户信息](./#access_token换取用户信息)  
    - [获取Admin用户列表](./#获取admin用户列表)  
    - [获取Admin用户详情](./#获取admin用户详情)  
    - [更新Admin用户信息](./#更新admin用户信息) 
    - [删除Admin用户](./#删除admin用户) 
    - [创建Admin用户](./#创建admin用户)  
- [产品模块](./#产品模块)  
    - [产品列表](./#产品列表)  
    - [产品新增](./#产品新增)  
    - [产品修改](./#产品修改)  
    - [产品禁用](./#产品禁用)  
- [随手花用户](./#随手花用户)  
    - [随手花用户列表](./#随手花用户列表)  
    - [随手花用户详情](./#随手花用户详情)  
    - [随手花用户禁用](./#随手花用户禁用)  
- [菜单](./#菜单)  
    - [获取菜单导航](./#获取菜单导航)
- [功能](./#功能)  
    - [上传文件到阿里云](./#上传文件到阿里云)  

    
### 测试主机host: 47.103.61.179:82/  

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
- 请求地址: {host}`get-access-token`
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
- 请求地址: {host}`admin/info`
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
### 获取Admin用户列表  
- 请求方式: `get`
- 请求地址: {host}`admins?type=1,2`
- 请求参数:  `type=1,2`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "name": "15061690110",
                "access_token": "o2iSTUyXyr0ij-1m22KAuToup00JaZ1S",
                "creater": null,
                "last_login_time": "2019-06-12 17:35:35",
                "last_login_ip": 2130706433,
                "register_time": null,
                "register_ip": null,
                "status": 1,
                "type": 1,
                "login_time": null
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8082/admins?name=15061690110&password=123456&page=1"
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

### 获取Admin用户详情  
- 请求方式: `get`
- 请求地址: {host}`admins/:id`
- 请求参数:  `:id`

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
        "type": 1,
        "login_time": null
    }
}
```

### 更新Admin用户信息  
- 请求方式: `put` or `patch`
- 请求地址: {host}`admins/:id`
- 请求参数:  `:id`
```json
{
    "name": "15061690110",
    "status": 1
}
```
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
        "type": 1,
        "login_time": null
    }
}
```

### 删除Admin用户  
- 请求方式: `delete`
- 请求地址: {host}`admins/:id`
- 请求参数:  `:id`

- 响应内容:  

```json
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```
### 创建Admin用户  
- 请求方式: `post`
- 请求地址: {host}`admins`
- 请求参数:  
```json
{
    "name": "你🐎死了",
    "password": "123456"
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "添加成功",
    "info": {
        "name": "13123",
        "access_token": "7DMeKgUny6d2D9E8dfTLJjkq5Jd6JRJC",
        "register_time": "2019-06-12 20:10:29",
        "register_ip": 2130706433,
        "last_login_ip": 2130706433,
        "last_login_time": "2019-06-12 20:10:29",
        "id": 8
    }
}
```
## 菜单
### 获取菜单导航  
- 请求方式: `get`
- 请求地址: {host}`admin/menu`
- 请求参数:  

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "1",
            "pid": "0",
            "title": "用户管理",
            "url": null,
            "icon": "el-icon-lx-people",
            "sort": "0",
            "status": "1",
            "subs": [
                {
                    "id": "2",
                    "pid": "1",
                    "title": "管理员列表",
                    "url": "adminlist",
                    "icon": null,
                    "sort": "0",
                    "status": "1"
                },
                {
                    "id": "3",
                    "pid": "1",
                    "title": "随手花用户",
                    "url": "userlist",
                    "icon": null,
                    "sort": "1",
                    "status": "1"
                }
            ]
        },
        {
            "id": "4",
            "pid": "0",
            "title": "产品",
            "url": null,
            "icon": "el-icon-document",
            "sort": "1",
            "status": "1",
            "subs": [
                {
                    "id": "5",
                    "pid": "4",
                    "title": "产品列表",
                    "url": "productlist",
                    "icon": null,
                    "sort": "0",
                    "status": "1"
                },
                {
                    "id": "6",
                    "pid": "4",
                    "title": "产品数据",
                    "url": "productdata",
                    "icon": null,
                    "sort": "1",
                    "status": "1"
                }
            ]
        },
        {
            "id": "7",
            "pid": "0",
            "title": "系统设置",
            "url": null,
            "icon": "el-icon-setting",
            "sort": "10",
            "status": "1",
            "subs": [
                {
                    "id": "8",
                    "pid": "7",
                    "title": "菜单管理",
                    "url": "menumanagement",
                    "icon": null,
                    "sort": "0",
                    "status": "1"
                },
                {
                    "id": "9",
                    "pid": "7",
                    "title": "用户组管理",
                    "url": "usergroupmanagement",
                    "icon": null,
                    "sort": "1",
                    "status": "1"
                }
            ]
        }
    ]
}
```
## 产品模块
### 产品列表  
- 请求方式: `get`
- 请求地址: {host}`products`
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
                "name": "随手花",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25458,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 1,
                "pass": 1,
                "sort": 10,
                "money": 499960,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 2,
                "name": "随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25462,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 0,
                "pass": 1,
                "sort": 11,
                "money": 499880,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 3,
                "name": "随dad花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 0,
                "pass": 1,
                "sort": 20,
                "money": 500000,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 4,
                "name": "随手花2gdsg",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 0,
                "pass": 1,
                "sort": 11,
                "money": 500000,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 5,
                "name": "rqwer手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25459,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 1,
                "hot": 0,
                "pass": 0,
                "sort": 19,
                "money": 499940,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 6,
                "name": "kk随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25457,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 1,
                "pass": 0,
                "sort": 121,
                "money": 499980,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 7,
                "name": "dDA手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25460,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 1,
                "hot": 1,
                "pass": 0,
                "sort": 11,
                "money": 499920,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 8,
                "name": "给个手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25459,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 1,
                "pass": 0,
                "sort": 12,
                "money": 499940,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 9,
                "name": "发送随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25456,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 0,
                "pass": 0,
                "sort": 13,
                "money": 500000,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 10,
                "name": "台湾随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25459,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 0,
                "pass": 0,
                "sort": 14,
                "money": 499940,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 11,
                "name": "约了随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25457,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 1,
                "hot": 0,
                "pass": 0,
                "sort": 2,
                "money": 499980,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 12,
                "name": "25随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25458,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 0,
                "hot": 0,
                "pass": 0,
                "sort": 1,
                "money": 499960,
                "status": 1,
                "user_price": 20,
                "platform": 1
            },
            {
                "id": 13,
                "name": "24随手花2",
                "image": "http://youloan.oss-cn-shanghai.aliyuncs.com/Uploads/2019-05-10/5cd4d64e8fc6a.png",
                "slogan": "易下款",
                "desc": "3分钟下款",
                "max_price": 50000,
                "apply_price": "2000-50000",
                "rate": "0.3%",
                "apply_num": 25464,
                "lending_time": 3,
                "max_duration": 14,
                "apply_duration": null,
                "url": "https://glhb.jiegezhima.com/ghb9/ghb.html?source=chuanqiqb",
                "new": 1,
                "hot": 1,
                "pass": 0,
                "sort": 0,
                "money": 499840,
                "status": 1,
                "user_price": 20,
                "platform": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8082/products?page=1"
            }
        },
        "_meta": {
            "totalCount": 13,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```
### 产品新增  
- 请求方式: `put` or `patch`
- 请求地址: {host}`products`
- 请求参数: 

```json  
{
	"name": "ceshi",
	"image": "images/product/71167f01gy1g1a54ny31zj20sg0lcdhs.jpg",
	"desc": "下快快",
	"max_price": 50000,
	"apply_price": "2000-50000",
	"rate": "0.03",
	"lending_time": "3",
	"max_duration": "15",
	"url": "http://baidu.com",
	"hot": 1,
	"sort": 0,
	"status": 1
}

```

- 响应内容:  

```json
{
    "code": 1,
    "message": "添加成功",
    "info": {
        "name": "13123",
        "access_token": "7DMeKgUny6d2D9E8dfTLJjkq5Jd6JRJC",
        "register_time": "2019-06-12 20:10:29",
        "register_ip": 2130706433,
        "last_login_ip": 2130706433,
        "last_login_time": "2019-06-12 20:10:29",
        "id": 8
    }
}
```
### 产品修改  
- 请求方式: `post`
- 请求地址: {host}`admins`
- 请求参数:  
```json
{
	"name": "ceshi",
	"image": "images/product/71167f01gy1g1a54ny31zj20sg0lcdhs.jpg",
	"desc": "下快快",
	"max_price": 50000,
	"apply_price": "2000-50000",
	"rate": "0.03",
	"lending_time": "3",
	"max_duration": "15",
	"url": "http://baidu.com",
	"hot": 1,
	"sort": 0,
	"status": 1
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "添加成功",
    "info": {
        "name": "13123",
        "access_token": "7DMeKgUny6d2D9E8dfTLJjkq5Jd6JRJC",
        "register_time": "2019-06-12 20:10:29",
        "register_ip": 2130706433,
        "last_login_ip": 2130706433,
        "last_login_time": "2019-06-12 20:10:29",
        "id": 8
    }
}
```
### 产品禁用  
- 请求方式: `delete`
- 请求地址: {host}`product/:id`
- 请求参数:  

- 响应内容:  

```json
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```

## 随手花用户  
### 随手花用户列表  
- 请求方式: `get`
- 请求地址: {host}`users?channel_id=1&active=0&start_time=2018-01-01 00:00:00&end_time=2019-10-10 00:00:00`
- 请求参数:  
- 说明: 筛选功能的时间为注册时间
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 79,
                "mobile": "15061690110",
                "access_token": "pUPOweZqcyPUVsMnz1LXNPTJZnvwnRIZ",
                "nick_name": null,
                "avatar_image": null,
                "register_time": "2019-06-03 15:26:05",
                "last_login_time": "2019-06-21 17:45:57",
                "register_ip": 2147483647,
                "last_login_ip": 2147483647,
                "status": 1,
                "active": 0,
                "active_time": null,
                "channel_id": 1,
                "package_id": null,
                "login_time": null
            },
            {
                "id": 80,
                "mobile": "15901725624",
                "access_token": "WhDSijD6Fuq6WPudUC0hqhQWe-HCVsX6",
                "nick_name": null,
                "avatar_image": null,
                "register_time": "2019-06-03 18:30:10",
                "last_login_time": "2019-06-17 15:20:30",
                "register_ip": 2147483647,
                "last_login_ip": 2147483647,
                "status": 1,
                "active": 0,
                "active_time": null,
                "channel_id": 1,
                "package_id": null,
                "login_time": null
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8082/users?channel_id=1&active=0&start_time=2018-01-01+00%3A00%3A00&end_time=2019-10-10+00%3A00%3A00&page=1"
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
### 随手花用户详情  

- 请求方式: `get`
- 请求地址: {host}`users/:id`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 80,
        "mobile": "15901725624",
        "access_token": "WhDSijD6Fuq6WPudUC0hqhQWe-HCVsX6",
        "nick_name": null,
        "avatar_image": null,
        "register_time": "2019-06-03 18:30:10",
        "last_login_time": "2019-06-17 15:20:30",
        "register_ip": 2147483647,
        "last_login_ip": 2147483647,
        "status": 1,
        "active": 0,
        "active_time": null,
        "channel_id": 1,
        "package_id": null,
        "login_time": null
    }
}
```

### 随手花用户禁用
- 请求方式: `delete`
- 请求地址: {host}`users/:id`
- 请求参数:  

- 响应内容:  

```json
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```


## 功能

### 上传文件到阿里云  
- 请求方式: `post`  
- 请求地址: {host}`upload-to-aliyun_oss`  
- 请求参数:  `file`  
- 响应内容:  

```json
{
    "code": 1,
    "message": "http://sshua.oss-cn-shanghai.aliyuncs.com/images/product/71167f01gy1g1a54ny31zj20sg0lcdhs.jpg",
    "info": {
        "url": "http://sshua.oss-cn-shanghai.aliyuncs.com/images/product/71167f01gy1g1a54ny31zj20sg0lcdhs.jpg",
        "content_type": null,
        "http_code": 200,
        "header_size": 334,
        "request_size": 467,
        "filetime": -1,
        "ssl_verify_result": 0,
        "redirect_count": 0,
        "total_time": 0.062,
        "namelookup_time": 0.015,
        "connect_time": 0.031,
        "pretransfer_time": 0.031,
        "size_upload": 36145,
        "size_download": 0,
        "speed_download": 0,
        "speed_upload": 582983,
        "download_content_length": 0,
        "upload_content_length": 36145,
        "starttransfer_time": 0.031,
        "redirect_time": 0,
        "redirect_url": "",
        "primary_ip": "106.14.228.186",
        "certinfo": [],
        "primary_port": 80,
        "local_ip": "192.168.5.191",
        "local_port": 55841,
        "method": "PUT"
    }
}
```
