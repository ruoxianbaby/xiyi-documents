## **用户端api**
<a href="./#用户端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [论坛](./#论坛)  
    - [栏目](./#栏目)   
    - [文章](./#文章)

### 测试主机host: 47.103.61.179:8074/  

### 全局header  

key |  vaule
----- | --------
Accept | application/json
Content-Type | application/json

需要验证的接口加上:  
  
key |  vaule
----- | --------
Authorization | Bearer ***access_token***  


## 论坛  
### 栏目  
- 请求方式: `get`
- 请求地址: `index.php?r=site%2Fcolumn`
- 响应内容:  
```json
{"status":1,"message":"success","info":[{"id":1,"name":"金融","status":1,"sort":1},{"id":2,"name":"推荐","status":1,"sort":1},{"id":3,"name":"科技","status":1,"sort":1},{"id":4,"name":"创业","status":1,"sort":1},{"id":5,"name":"内幕","status":1,"sort":1}]}
```
### 文章  
- 请求方式: `get`
- 请求地址: `index.php?r=site%2Farticle`
- 响应内容:  


