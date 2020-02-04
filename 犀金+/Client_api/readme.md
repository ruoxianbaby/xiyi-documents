## **用户端api**
<a href="./#用户端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [加盟宝](./#加盟宝)
    - [首页分类](./#首页分类)  
    - [首页热门专区](./#首页热门专区)
    - [首页热门推荐](./#首页热门推荐)
    - [所有分类](./#所有分类)  
    - [加盟宝详情](./#加盟宝详情)  
    - [加盟宝某个分类列表](./#加盟宝某个分类列表)  

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

### 首页热门推荐  
- 请求方式: `get`
- 请求地址: `jmbs?is_hot_recommend=1?per-page=50`
- 请求参数:  
per-page=50 写死
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
                "name": "和府捞面2",
                "direct_store_num": "121234",
                "apply_num": "11111",
                "join_fee": "10-25万",
                "image_url": "https://www.baidu.com",
                "category_name": "餐饮",
                "brand_year": "6"   年限
            },
            {
                "name": "和府捞面",
                "direct_store_num": "121234",
                "apply_num": "11111",
                "join_fee": "10-25万",
                "image_url": "https://www.baidu.com",
                "category_name": "餐饮",
                "brand_year": "6"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmbs?is_hot_recommend=1%3Fper-page%3D50&page=1"
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


### 所有分类  
- 请求方式: `get`
- 请求地址: `jmb/get-category`
- 请求参数:  

- 响应内容:  
注：
image_url 在第一层是没有意义的，在第二层category_child,category_brand用来展示logo
category_child中点进去用id,点进去的接口  jmbs?jmb_category_id=5  （这个分类中所有的加盟宝列表 - 转到加盟宝某个分类列表）
category_brand中点进去用id,点进去的接口  jmb/detail?id=1  （加盟宝详情接口） 
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "0",  在热门这 此处没有意义
            "image_url": "",   在热门这 此处没有意义
            "name": "热门",
            "category_child": [],  热门没有该项，请看设计图
            "category_brand": [
                {
                    "id": "1",
                    "name": "和府捞面", 
                    "image_url": "https://www.baidu.com"
                },
                {
                    "id": "2",
                    "name": "和府捞面2",
                    "image_url": "https://www.baidu.com"
                }
            ]
        },
        {
            "id": "1",
            "name": "餐饮",
            "image_url": "",
            "category_child": [
                {
                    "id": "5",
                    "name": "快餐1",
                    "image_url": ""
                },
                {
                    "id": "6",
                    "name": "快餐22",
                    "image_url": ""
                }
            ],
            "category_brand": [
                {
                    "id": "1",
                    "name": "和府捞面",
                    "image_url": "https://www.baidu.com"
                },
                {
                    "id": "2",
                    "name": "和府捞面2",
                    "image_url": "https://www.baidu.com"
                }
            ]
        },
        {
            "id": "2",
            "name": "教育",
            "image_url": "",
            "category_child": [],
            "category_brand": []
        },
        {
            "id": "3",
            "name": "酒店",
            "image_url": "",
            "category_child": [],
            "category_brand": []
        },
        {
            "id": "4",
            "name": "早教",
            "image_url": "",
            "category_child": [],
            "category_brand": []
        }
    ]
}
```


### 加盟宝详情  
- 请求方式: `get`
- 请求地址: `jmb/detail?id=1`
- 请求参数:  

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": "1",
                "name": "和府捞面",
                "jmb_category_id": "5",
                "brand_name": "品牌123",
                "desc": "描述",
                "direct_store_num": "121234",
                "join_store_num": "222",
                "apply_num": "11111",
                "main_project": "餐饮、文化、面、点心",
                "register_time": "2014年",
                "location": "上海",
                "est_init_investment": "10-25万",
                "est_customer_unit_price": "45元/人",
                "est_customer_daily_flow": "121人/日",
                "est_mothly_sale": "14万",
                "est_gross_profit": "50%",
                "est_payback_period": "3-6月",
                "inital_fee": "15",
                "join_fee": "10-25万",
                "deposit_fee": "5万",
                "device_fee": "无",
                "other_fee": "无",
                "is_hot_join": "1",
                "is_hot_recommend": "1",
                "image_url": "https://www.baidu.com",
                "info": "富文本内容",
                "create_time": "2020-02-03 15:11:27",
                "update_time": null,
                "category_name": "餐饮",
                "brand_year": "6"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmb/detail?id=1&page=1"
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

  `name` '加盟宝名称',
  `jmb_category_id`  '分类id',
  `brand_name` '品牌名称',
  `desc` '描述',
  `direct_store_num`'直营店数量',
  `join_store_num` '加盟店数量',
  `apply_num`  '申请加盟数量',
  `main_project` '主营项目',
  `register_time` '品牌注册时间',
  `location` '公司所在地',
  `est_init_investment` '预估初始投资',
  `est_customer_unit_price` '预估客单价',
  `est_customer_daily_flow` '预估日客流量',
  `est_mothly_sale` '预估月销售额',
  `est_gross_profit` '预估毛利润',
  `est_payback_period`  '预估回报周期',
  `inital_fee` '初期预计投入',
  `join_fee` '加盟费',
  `deposit_fee`  '保证金',
  `device_fee` '设备费用',
  `other_fee`  '其他费用',
  `info` text COMMENT '富文本内容',
```


### 加盟宝某个分类列表  
- 请求方式: `get`
- 请求地址: `jmbs?jmb_category_id=5&page=1&per-page=20`
- 请求参数:  
注 这个是有分页的
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "name": "和府捞面",
                "direct_store_num": "121234",
                "apply_num": "11111",
                "join_fee": "10-25万",
                "image_url": "https://www.baidu.com",
                "category_name": "餐饮",
                "brand_year": "6"   年限
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmbs?jmb_category_id=5&page=1"
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
