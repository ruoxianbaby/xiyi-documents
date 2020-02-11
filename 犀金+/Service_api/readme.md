## **后台api**
<a href="./#后台api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [加盟宝](./#加盟宝)
    - [banner图一套restful](./#banner图一套restful)  
    - [获得广告图片](./#获得广告图片) 
    - [广告图片修改](./#广告图片修改)
    - [热门专区一套restful](./#热门专区一套restful)

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

### banner图一套restful
- 请求方式: `get`
- 请求地址: `jmb-banners`
- 请求参数:  
restful 风格一套   
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 1,
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
                "type": 1,
                "jmb_id": 1,
                "use_out_link": 0,
                "out_link_url": ""
            },
            {
                "id": 2,
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
                "type": 1,
                "jmb_id": 0,
                "use_out_link": 1,
                "out_link_url": "https://www.baidu.com"
            },
            {
                "id": 3,
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
                "type": 1,
                "jmb_id": 2,
                "use_out_link": 0,
                "out_link_url": ""
            },
            {
                "id": 4,
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
                "type": 1,
                "jmb_id": 3,
                "use_out_link": 0,
                "out_link_url": ""
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_service.com/jmb-banners?page=1"
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
use_out_link : 如果是1 那么就使用外部链接out_link_url
是0 ：点击图片跳转jmb_id对应详情
use_out_link可以做个√ x之类的啥的吧
```



### 获得广告图片  
- 请求方式: `get`
- 请求地址: `jmb-banner/get-ad`
- 请求参数:  
   
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": "5",
        "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
        "type": "2",
        "jmb_id": "4",
        "use_out_link": "0",
        "out_link_url": ""
    }
}
use_out_link : 如果是1 那么就使用外部链接out_link_url
是0 ：点击图片跳转jmb_id对应详情
```


### 广告图片修改  
- 请求方式: `post`
- 请求地址: `jmb-banner/edit-ad`
- 请求参数:  
不用给我id
```json
{
    "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
    "jmb_id": "4",
    "use_out_link": "0",
    "out_link_url": ""
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "id": "5",
        "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
        "type": "2",
        "jmb_id": "4",
        "use_out_link": "0",
        "out_link_url": ""
    }
}
```




### 热门专区一套restful  
- 请求方式: `get`
- 请求地址: `jmb-hot-prefectures`
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
                "jmb_category_id": 5,
                "name": "餐饮美食",
                "desc": "原料，店面设计的支持",
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
            },
            {
                "id": 2,
                "jmb_category_id": 6,
                "name": "快餐22",
                "desc": "原料，店面设计的支持",
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
            },
            {
                "id": 3,
                "jmb_category_id": 7,
                "name": "子教育xxx",
                "desc": "原料，店面设计的支持",
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_service.com/jmb-hot-prefectures?page=1"
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