## **服务端api**
<a href="./#服务端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [用户模块](./#用户模块)  
    - [获取access_token](./#获取access_token)  
    - [access_token换取用户信息](./#access_token换取用户信息)  
    - [获取用户列表](./#获取用户列表)  
    - [获取用户信息](./#获取用户信息)  
    - [更新用户信息](./#更新用户信息) 
    - [删除用户](./#删除用户) 
    - [创建用户](./#创建用户)
- [菜单](./#菜单)  
    - [获取菜单导航](./#获取菜单导航)
    
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
### 获取用户列表 
- 请求方式: `get`
- 请求地址: {host}`admins`
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

### 获取用户信息 
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

### 更新用户信息 
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

### 删除用户 
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
### 创建用户 
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
