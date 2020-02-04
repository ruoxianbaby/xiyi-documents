## **用户端api**
<a href="./#用户端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [加盟宝](./#加盟宝)  
    - [首页热门专区](./#首页热门专区)

### 测试主机host: 47.103.61.179:1022/  

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
### 首页热门专区  
- 请求方式: `get`
- 请求地址: `jmb/get-hot-prefecture?per-page=5`
- 请求参数:
per-page=5 写死
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
                "id": "1",
                "jmb_category_id": "5",
                "name": "餐饮美食",
                "desc": "原料，店面设计的支持",
                "image_url": ""
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmb/get-hot-prefecture?per-page=5&page=1"
            }
        },
        "_meta": {
            "totalCount": 1,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 5
        }
    }
}
```
