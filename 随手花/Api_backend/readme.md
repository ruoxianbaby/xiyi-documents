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
    - [产品详情](./#产品详情)  
    - [产品新增](./#产品新增)  
    - [产品修改](./#产品修改)  
    - [产品禁用](./#产品禁用)  
    - [产品流量扣除](./#产品流量扣除)  
- [随手花用户](./#随手花用户)  
    - [随手花用户列表](./#随手花用户列表)  
    	- [用于筛选用户的渠道](./#用于筛选用户的渠道)
    - [随手花用户详情](./#随手花用户详情)  
    - [随手花用户禁用](./#随手花用户禁用)  
- [渠道模块](./#渠道模块)
    - [渠道列表](./#渠道列表)
    - [渠道详情](./#渠道详情)
    - [渠道新增](./#渠道新增)
    - [渠道修改](./#渠道修改)
    - [渠道删除](./#渠道删除)  
    - [渠道所属系统](./#渠道所属系统)
- [菜单](./#菜单)  
    - [获取菜单导航](./#获取菜单导航)
- [功能](./#功能)  
    - [上传文件到阿里云](./#上传文件到阿里云)  
- [扣量模块](./#扣量模块)
    - [扣量列表](./#扣量列表)
    - [扣量详情](./#扣量详情)
    - [扣量新增](./#扣量新增)
    - [扣量修改](./#扣量修改)
    - [扣量删除](./#扣量删除)
- [数据统计模块](./#数据统计模块)
    - [今日实时PV/UV](./#今日实时PV/UV)
    - [产品每日统计](./#产品每日统计)
    - [渠道每日统计-实时](./#渠道每日统计-实时)
    - [渠道每日统计-历史](./#渠道每日统计-历史)  
    - [用户申请记录-列表](./#用户申请记录-列表)
    - [用户申请记录-申请人数](./#用户申请记录-申请人数)  
- [刷单检测](./#刷单检测)
- [首页数据统计模块](./#首页数据统计模块)
    - [今日实时](./#今日实时)
    - [用户统计](./#用户统计)
    - [七日趋势](./#七日趋势)  
    - [今日渠道转化](./#今日渠道转化)  
    
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
    "name": "name",
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
### 产品详情
- 请求方式: `get`
- 请求地址: {host}`products/:id`
- 请求参数: `id`
- 响应内容:
```json  
{
    "code": 1,
    "message": "success",
    "info": {
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
        "status": 0,
        "user_price": 20,
        "platform": 1,
        "create_time": null
    }
}	
```

### 产品新增  
- 请求方式: `post`
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
    "message": "创建成功",
    "info": {
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
        "status": 1,
        "id": 17
    }
}
```
### 产品修改  
- 请求方式: `put` or `patch`
- 请求地址: {host}`products/:id`
- 请求参数:  
```json
{
    "name": "传奇钱包"
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 1,
        "name": "传奇钱包",
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
        "status": 0,
        "user_price": 20,
        "platform": 1,
        "create_time": null
    }
}
```
### 产品禁用  
- 请求方式: `delete`
- 请求地址: {host}`/product/:id`
- 请求参数:  

- 响应内容:  

```json
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```

### 产品流量扣除  
- 请求方式: `post`
- 请求地址: {host}`/product/deduct`
- 请求参数:  product_id  num  price

- 响应内容:  

```json
{
    "code": 1,
    "message": "新增成功",
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

####  用于筛选用户的渠道
参照 [渠道列表](./#渠道列表)  

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

## 渠道模块
### 渠道列表

- 请求方式: `get`
- 请求地址: {host}`channels`
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
                "name": "包总",
                "channel_sign": null,
                "url": "http://www.baidu.com",
                "admin_id": 1,
                "cooperation_type": 1,
                "qrcode": "1",
                "status": 1,
                "app_url": "1",
                "create_time": "2019-06-17 13:42:07",
                "creater_id": 0
            },
            {
                "id": 2,
                "name": "包总2",
                "channel_sign": null,
                "url": "http://www.baidu.com",
                "admin_id": 1,
                "cooperation_type": 1,
                "qrcode": "1",
                "status": 1,
                "app_url": "1",
                "create_time": "2019-06-17 13:42:07",
                "creater_id": 0
            },
            {
                "id": 3,
                "name": "baozong",
                "channel_sign": null,
                "url": "http://m.sshua.com/channel/user?channel_sign=bMslBvgo-CUwbR2Pzu1XrXedRRyYU_RT",
                "admin_id": 80,
                "cooperation_type": 1,
                "qrcode": "images/qrcode/bMslBvgo-CUwbR2Pzu1XrXedRRyYU_RT.png",
                "status": 1,
                "app_url": "sshua.com",
                "create_time": "2019-06-27 10:49:36",
                "creater_id": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://47.103.61.179:82/channels?page=1"
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

### 渠道详情  
- 请求方式: `get`
- 请求地址: {host}`channels/:id`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 2,
        "name": "包总2",
        "channel_sign": null,
        "url": "http://www.baidu.com",
        "admin_id": 1,
        "cooperation_type": 1,
        "qrcode": "1",
        "status": 1,
        "app_url": "1",
        "create_time": "2019-06-17 13:42:07",
        "creater_id": 0
    }
}
```
### 渠道新增
- 请求方式: `post`
- 请求地址: {host}`channels`
- 请求参数:  
```json
{
    "name": "baozong",
    "admin_id": 80,
    "cooperation_type": 1,
    "app_url": "www.baidu.com"
}
```
- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "name": "baozong",
        "admin_id": 80,
        "cooperation_type": 1,
        "app_url": "www.baidu.com",
        "creater_id": 1,
        "channel_sign": "SVQh5SiymVQ1IMw5H9Pu4hm7Y3YpopJ0",
        "url": "http://m.sshua.com/channel/user?channel_sign=SVQh5SiymVQ1IMw5H9Pu4hm7Y3YpopJ0",
        "qrcode": "images/qrcode/SVQh5SiymVQ1IMw5H9Pu4hm7Y3YpopJ0.png",
        "create_time": "2019-06-28 13:38:00",
        "id": 6
    }
}
```
### 渠道修改
- 请求方式: `put` or `patch`
- 请求地址: {host}`localhost:8082/channels/:id`
- 请求参数:  
```json
{
    "name": "baozong",
    "admin_id": 80,
    "cooperation_type": 1,
    "app_url": "www.baidu.com"
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 5,
        "name": "baozong",
        "channel_sign": "RIyQBWf2jzWsKnTDAv4BqpTyJntf8j2o",
        "url": "http://m.sshua.com/channel/user?channel_sign=RIyQBWf2jzWsKnTDAv4BqpTyJntf8j2o",
        "admin_id": 80,
        "cooperation_type": 1,
        "qrcode": "images/qrcode/RIyQBWf2jzWsKnTDAv4BqpTyJntf8j2o.png",
        "status": 1,
        "app_url": "www.baidu.com",
        "create_time": "2019-06-28 13:34:25",
        "creater_id": 1
    }
}
```

### 渠道删除
- 请求方式: `delete`
- 请求地址: {host}`channels/:id`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```

### 渠道所属系统
- 请求方式: `get`
- 请求地址: {host}`channel/platform`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "",
    "info": [
        {
            "id": 9,
            "name": "自研系统"
        },
        {
            "id": 8,
            "name": "非凡"
        },
        {
            "id": 7,
            "name": "牛顿"
        },
        {
            "id": 6,
            "name": "晟盾"
        },
        {
            "id": 5,
            "name": "胡萝卜"
        },
        {
            "id": 4,
            "name": "新脉"
        },
        {
            "id": 3,
            "name": "战盾"
        },
        {
            "id": 2,
            "name": "指维"
        },
        {
            "id": 1,
            "name": "新贝途"
        }
    ]
}
```

## 功能

### 上传文件到阿里云  
- 请求方式: `post`  
- 请求地址: {host}`upload-to-aliyun_oss?type=product`  
- 请求参数:  `file` 
- 说明: `type`字段 代表上传到不同的文件夹,对应关系如下:
```json
{
    "product": "/product/images",
    "banner": "/banner/images",
    ...
}
```  

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

## 扣量模块
### 扣量列表

- 请求方式: `get`
- 请求地址: {host}`/deducts`
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
                "channel_id": 1,
                "deduct": 0.8,
                "date_time": "2019-07-01",
                "create_time": "2019-07-01 14:04:10",
                "status": 0,
                "channel_name": "包总"
            },
            {
                "id": 4,
                "channel_id": 1,
                "deduct": 0.8,
                "date_time": "2019-07-01",
                "create_time": "2019-07-01 14:04:10",
                "status": 1,
                "channel_name": "包总"
            }
        ],
        "_links": {
            "self": {
                "href": "http://ssh.org:82/deducts?per-page=3&page=1"
            },
            "next": {
                "href": "http://ssh.org:82/deducts?per-page=3&page=2"
            },
            "last": {
                "href": "http://ssh.org:82/deducts?per-page=3&page=3"
            }
        },
        "_meta": {
            "totalCount": 9,
            "pageCount": 3,
            "currentPage": 1,
            "perPage": 3
        }
    }
}
```  

### 扣量详情  
- 请求方式: `get`
- 请求地址: {host}`/deducts/:id`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 1,
        "channel_id": 1,
        "deduct": 0.8,
        "date_time": "2019-07-01",
        "create_time": "2019-07-01 14:04:10",
        "status": 0
    }
}
```
### 扣量新增
- 请求方式: `post`
- 请求地址: {host}`/deducts`
- 请求参数:  
```json

{
    "code": 1,
    "message": "创建成功",
    "info": {
	    "channel_id": 1,
	    "deduct": 0.8,
	    "date_time": "2019-06-30",
	    "status": 1
	}
}
```
- 响应内容:  

```json  
{
    "code": 1,
    "message": "操作成功",
    "info": {
        "channel_id": "31",
        "deduct": "0.7",
        "date_time": "2019-06-30",
        "create_time": "2019-07-01 16:54:17",
        "id": 12
    }
}
```
### 扣量修改
- 请求方式: `put` or `patch`
- 请求地址: {host}`/deducts/:id`
- 请求参数:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
	"channel_id":8,
	"deduct":0.71,
	"date_time":"2019-06-30"
    }
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": 1,
        "channel_id": 8,
        "deduct": 0.71,
        "date_time": "2019-06-30",
        "create_time": "2019-07-01 14:04:10",
        "status": 0
    }
}
```

### 扣量删除
- 请求方式: `delete`
- 请求地址: {host}`deducts/:id`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```

## 数据统计模块
### 今日实时PV/UV

- 请求方式: `get`
- 请求地址: {host}`/channel-analysis/today-count`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "Success",
    "info": {
        "pv": "16",
        "uv": "3"
    }
}
```  

### 产品每日统计

- 请求方式: `get`
- 请求地址: {host}`/channel-analysis/day-count`
- 请求参数: 

- 响应内容:  
pv -> 注册按钮点击pv  
pv_total -> 注册按钮点击累积pv  
uv -> 注册按钮点击uv  
uv_total -> 注册按钮点击累积uv  
new_ctr_uv -> 新客uv  
old_ctr_uv -> 老客uv  
balance_type -> 结算方式 1:uv, 2:cpa, 3cps  
user_price -> 结算单价  
income -> 收益

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 24,
                "product_id": 5,
                "pv": 4,
                "pv_total": 4,
                "uv": 2,
                "uv_total": 2,
                "create_time": "2019-07-09 17:24:36",
                "date": "2019-07-08",
                "new_ctr_uv": 1,
                "old_ctr_uv": 0,
                "balance_type": 1,
                "user_price": null,
                "product_name": "",
                "income": 0
            },
            {
                "id": 23,
                "product_id": 1,
                "pv": 1,
                "pv_total": 1,
                "uv": 1,
                "uv_total": 1,
                "create_time": "2019-07-09 17:09:27",
                "date": "2019-07-08",
                "new_ctr_uv": 0,
                "old_ctr_uv": 0,
                "balance_type": null,
                "user_price": null,
                "product_name": "",
                "income": 0
            }
        ],
        "_links": {
            "self": {
                "href": "http://ssh.org:82/channel-analysis/day-count?page=2"
            },
            "first": {
                "href": "http://ssh.org:82/channel-analysis/day-count?page=1"
            },
            "prev": {
                "href": "http://ssh.org:82/channel-analysis/day-count?page=1"
            }
        },
        "_meta": {
            "totalCount": 22,
            "pageCount": 2,
            "currentPage": 2,
            "perPage": 20
        }
    }
}
```  

### 渠道每日统计-实时

- 请求方式: `get`
- 请求地址: {host}`/channel-analysis/today-list`
- 请求参数: 

- 响应内容:  
	reg - 注册数  
	active - 激活数  
	p_uv - 产品点击uv  
	p_pv - 产品点击pv  
	uv - 渠道uv
	
```json  
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "channel_id": "1",
            "channel_name": "包总",
            "reg": 0,
            "active": 0,
            "p_uv": 0,
            "p_pv": 0,
            "uv": 0
        },
        {
            "channel_id": "2",
            "channel_name": "包总2",
            "reg": 0,
            "active": 0,
            "p_uv": 0,
            "p_pv": 0,
            "uv": 0
        }
    ]
}
```  

### 渠道每日统计-历史

- 请求方式: `get`
- 请求地址: {host}`/channel-analysis/day-list?channel_name=包总&start_time=2019-07-01&end_time=2019-07-03`
- 请求参数: channel_name, start_time, end_time

- 响应内容:  
	channel_name - 渠道名称  
	date - 统计日期  
	uv - 推广页uv  
	reg - 渠道注册  
	active - 渠道激活  
	p_pv - 产品pv(新客)  
	p_uv - 产品uv(新客)  
	p_old_pv - 产品pv(老客)  
	p_old_uv - 产品uv(老客)  
	reg_uv_pre - 注册转化率  
	active_uv_pre - 激活转化率  
	p_uv_uv_pre - 新客转化率  
```json  
{
    "code": 1,
    "message": "Success",
    "info": {
        "1": {
            "channel_name": "包总",
            "list": [
                {
                    "channel_id": "1",
                    "uv": "1",
                    "reg": "2",
                    "active": "2",
                    "p_uv": "0",
                    "p_pv": "0",
                    "p_old_uv": "0",
                    "p_old_pv": "0",
                    "reg_uv_pre": "0.00",
                    "active_uv_pre": "0.00",
                    "p_uv_uv_pre": "0.00",
                    "date": "2019-07-01",
                    "channel_name": "包总"
                },
                {
                    "channel_id": "1",
                    "uv": "2",
                    "reg": "1",
                    "active": "0",
                    "p_uv": "0",
                    "p_pv": "0",
                    "p_old_uv": "0",
                    "p_old_pv": "0",
                    "reg_uv_pre": "50.00",
                    "active_uv_pre": "0.00",
                    "p_uv_uv_pre": "0.00",
                    "date": "2019-07-02",
                    "channel_name": "包总"
                }
            ]
        },
        "2": {
            "channel_name": "包总2",
            "list": [
                {
                    "channel_id": "2",
                    "uv": "1",
                    "reg": "0",
                    "active": "0",
                    "p_uv": "1",
                    "p_pv": "1",
                    "p_old_uv": "0",
                    "p_old_pv": "0",
                    "reg_uv_pre": "0.00",
                    "active_uv_pre": "0.00",
                    "p_uv_uv_pre": "0.00",
                    "date": "2019-07-01",
                    "channel_name": "包总2"
                },
                {
                    "channel_id": "2",
                    "uv": "2",
                    "reg": "0",
                    "active": "0",
                    "p_uv": "0",
                    "p_pv": "0",
                    "p_old_uv": "1",
                    "p_old_pv": "1",
                    "reg_uv_pre": "0.00",
                    "active_uv_pre": "0.00",
                    "p_uv_uv_pre": "0.00",
                    "date": "2019-07-02",
                    "channel_name": "包总2"
                }
            ]
        }
    }
}
```  

### 用户申请记录-列表

- 请求方式: `get`
- 请求地址: {host}`/apply-record/index`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 599,
                "user_id": 82,
                "channel_id": 2,
                "product_id": 13,
                "apply_time": "2019-07-02 14:57:36",
                "ip": 2147483647,
                "mobile": "18308461696",
                "product_name": "24随手花2"
            },
            {
                "id": 598,
                "user_id": 82,
                "channel_id": null,
                "product_id": 13,
                "apply_time": "2019-07-02 14:30:50",
                "ip": 2147483647,
                "mobile": "18308461696",
                "product_name": "24随手花2"
            }
        ],
        "_links": {
            "self": {
                "href": "http://ssh.org:82/apply-record/index?page=1"
            },
            "next": {
                "href": "http://ssh.org:82/apply-record/index?page=2"
            },
            "last": {
                "href": "http://ssh.org:82/apply-record/index?page=30"
            }
        },
        "_meta": {
            "totalCount": 599,
            "pageCount": 30,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```  

### 用户申请记录-申请人数

- 请求方式: `get`
- 请求地址: {host}`/apply-record/count`
- 请求参数:  

- 响应内容:  

```json  
{
    "code": 1,
    "message": "Success",
    "info": {
        "total_num": "16",
        "today_num": "0"
    }
}
```  

### 刷单检测
- 请求方式: `get`
- 请求地址: {host}`click-farms?sort=-id`

- 响应内容:  

```json  
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "create_time": "2019-07-01 17:48:45",
                "mobile": "15061690110",
                "user_id": null,
                "channel_id": null,
                "ip": "192.168.1.66"
            },
            {
                "id": 3,
                "create_time": "2019-07-01 15:00:42",
                "mobile": "15901725624",
                "user_id": null,
                "channel_id": null,
                "ip": "192.168.1.36"
            },
            {
                "id": 4,
                "create_time": null,
                "mobile": null,
                "user_id": null,
                "channel_id": null,
                "ip": "192.168.1.63"
            },
            {
                "id": 5,
                "create_time": null,
                "mobile": null,
                "user_id": null,
                "channel_id": null,
                "ip": "192.168.1.78"
            }
        ],
        "_links": {
            "self": {
                "href": "http://localhost:8082/click-farms?name=15061690111&password=123456&page=1"
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

## 首页数据统计模块
### 今日实时

- 请求方式: `get`
- 请求地址: {host}`/index/index`
- 请求参数:  

- 响应内容:  
user_total -> 总用户人数  
user_new -> 今日新增用户数  
pdt_uv -> 今日产品UV  
act_uv -> 新客UV  
click_farm -> 今日刷单数  
last_pdt_uv -> 昨日产品UV  
pre -> 今日UV效率  
last_pre -> 昨日UV效率  

```json  
{
    "code": 1,
    "message": "Success",
    "info": {
        "user_total": "8",
        "user_new": "3",
        "pdt_uv": "1",
        "act_uv": "0",
        "click_farm": "0",
        "last_pdt_uv": "26",
        "pre": "25.00",
        "last_pre": "2600.00"
    }
}
```  

### 用户统计

- 请求方式: `get`
- 请求地址: {host}`/index/user`
- 请求参数:  

- 响应内容:  
latent -> 意向用户  
total_black -> 黑名单用户  
very_black -> 极黑用户  

```json  
{
    "code": 1,
    "message": "Success",
    "info": {
        "very_black": "13380",
        "total_black": "33917",
        "latent": "247908"
    }
}
```  

### 七日趋势

- 请求方式: `get`
- 请求地址: {host}`/index/channel-analysis`
- 请求参数:  

- 响应内容:  
```json  
{
    "code": 1,
    "message": "Success",
    "info": [
        [
            {
                "date": "2019-07-01",
                "name": "推广页UV",
                "value": "2"
            },
            {
                "date": "2019-07-01",
                "name": "推广页注册数",
                "value": "2"
            },
            {
                "date": "2019-07-01",
                "name": "渠道激活数",
                "value": "2"
            },
            {
                "date": "2019-07-01",
                "name": "产品新客UV数",
                "value": "2"
            }
        ],
        [
            {
                "date": "2019-07-02",
                "name": "推广页UV",
                "value": "6"
            },
            {
                "date": "2019-07-02",
                "name": "推广页注册数",
                "value": "1"
            },
            {
                "date": "2019-07-02",
                "name": "渠道激活数",
                "value": "0"
            },
            {
                "date": "2019-07-02",
                "name": "产品新客UV数",
                "value": "0"
            }
        ],
        [
            {
                "date": "2019-07-03",
                "name": "推广页UV",
                "value": "2"
            },
            {
                "date": "2019-07-03",
                "name": "推广页注册数",
                "value": "0"
            },
            {
                "date": "2019-07-03",
                "name": "渠道激活数",
                "value": "0"
            },
            {
                "date": "2019-07-03",
                "name": "产品新客UV数",
                "value": "23"
            }
        ],
        [
            {
                "date": "2019-07-04",
                "name": "推广页UV",
                "value": "2"
            },
            {
                "date": "2019-07-04",
                "name": "推广页注册数",
                "value": "2"
            },
            {
                "date": "2019-07-04",
                "name": "渠道激活数",
                "value": "1"
            },
            {
                "date": "2019-07-04",
                "name": "产品新客UV数",
                "value": "1"
            }
        ]
    ]
}
```  

### 今日渠道转化

- 请求方式: `get`
- 请求地址: {host}`/index/channels`
- 请求参数:  

- 响应内容:  
```json  
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "name": "推广页UV",
            "value": 3,
            "washaway": 0.3333333333333333
        },
        {
            "name": "推广页注册",
            "value": 1,
            "washaway": 1
        },
        {
            "name": "激活",
            "value": 1
        }
    ]
}
```  
