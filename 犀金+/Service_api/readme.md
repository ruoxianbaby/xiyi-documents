## **后台api**
<a href="./#后台api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [加盟宝](./#加盟宝)
    - [首页分类](./#首页分类)  

### 测试主机host: 47.103.61.179:1081/  

### 全局header  

key |  vaule
----- | --------
Accept | application/json
Content-Type | application/json

需要验证的接口加上:  

key |  vaule
----- | --------
Authorization | Bearer ***access_token***  


## 加盟宝  

### 首页分类  
- 请求方式: `get`
- 请求地址: `jmb/get-home-category`
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
            "name": "餐饮",
            "image_url": ""
        },
        {
            "id": "2",
            "pid": "0",
            "name": "教育",
            "image_url": ""
        },
        {
            "id": "3",
            "pid": "0",
            "name": "酒店",
            "image_url": ""
        },
        {
            "id": "4",
            "pid": "0",
            "name": "早教",
            "image_url": ""
        }
    ]
}
```
