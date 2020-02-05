## **用户端api**
<a href="./#用户端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [加盟宝](./#加盟宝)
    - [首页分类](./#首页分类)  
    - [首页热门专区](./#首页热门专区)
    - [热门专区全部](./#热门专区全部)
    - [首页热门推荐](./#首页热门推荐)
    - [所有分类](./#所有分类)  
    - [加盟宝详情](./#加盟宝详情)  
    - [加盟宝某个分类列表](./#加盟宝某个分类列表)  
    - [加盟宝投资金额搜索](./#加盟宝投资金额搜索)  
    - [加盟宝评论](./#加盟宝评论)  
    - [加盟宝评论页面](./#加盟宝评论页面)  
    - [加盟宝评论详情](./#加盟宝评论详情)  
    - [加盟宝评论点赞](./#加盟宝评论点赞)  
    - [获取加盟方式](./#获取加盟方式)  
    - [我的加盟](./#我的加盟)

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


### 热门全部  
- 请求方式: `get`
- 请求地址: `jmb/get-hot-prefecture?page=1&per-page=20`
- 请求参数:  
注：带分页
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
                "est_init_investment": "10-25万",
                "image_url": "https://www.baidu.com",
                "category_name": "餐饮",
                "brand_year": "6"   年限
            },
            {
                "name": "和府捞面",
                "direct_store_num": "121234",
                "apply_num": "11111",
                "est_init_investment": "10-25万",
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
category_child中点进去用id,点进去的接口  jmbs?jmb_category_id=5  （这个分类中所有的加盟宝列表 - 转到加盟宝某个分类列表）(./#加盟宝某个分类列表)  
category_brand中点进去用id,点进去的接口  jmb/detail?id=1  （加盟宝详情接口）(./#加盟宝详情)    
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
                "est_init_investment": "10-25万",
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

### 加盟宝评论  
- 请求方式: `post`
- 请求地址: `jmb-comments`
- 请求参数:  
```json
{
	"id": 1,
	"content":"还不错",
	"pid": 0    0是评论加盟宝,非0是评论其他
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "添加成功",
    "info": {
        "id": 4,
        "jmb_id": 1,
        "content": "还不错",
        "create_time": "2020-02-04 16:59:47",
        "user_id": 1,
        "pid": 3,
        "reply_pid": 3,
        "nick_name": "微微笑",
        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
        "time_before": "刚刚"
    }
}
```



### 加盟宝评论页面  
- 请求方式: `get`
- 请求地址: `jmb-comments?jmb_id=1`
- 请求参数:  jmb_id 是当前加盟宝详情页的加盟宝id

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": "1",
                "jmb_id": "1",
                "user_id": "1",
                "content": "还不错",
                "pid": "0",
                "reply_pid": "0",
                "like_num": "1",
                "create_time": "2020-02-04 17:47:52",
                "update_time": null,
                "nick_name": "微微笑",
                "user_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "30分钟前",
                "like": "0",
                "like_count": "0",
                "child": []
            },
            {
                "id": "2",
                "jmb_id": "1",
                "user_id": "1",
                "content": "还不错",
                "pid": "0",
                "reply_pid": "0",
                "like_num": "0",
                "create_time": "2020-02-04 16:57:16",
                "update_time": null,
                "nick_name": "微微笑",
                "user_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "1小时前",
                "like": "0",
                "like_count": "0",
                "child": []
            },
            {
                "id": "3",
                "jmb_id": "1",
                "user_id": "1",
                "content": "还不错",
                "pid": "0",
                "reply_pid": "0",
                "like_num": "0",
                "create_time": "2020-02-04 16:57:35",
                "update_time": null,
                "nick_name": "微微笑",
                "user_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "1小时前",
                "like": "0",
                "like_count": "0",
                "child": [
                    {
                        "id": "4",
                        "jmb_id": "1",
                        "user_id": "2",
                        "content": "还不错",
                        "pid": "3",
                        "reply_pid": "3",
                        "like_num": "1",
                        "create_time": "2020-02-04 16:59:47",
                        "update_time": null,
                        "time_before": "1小时前",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/50939351.jpg",
                        "nick_name": "陌南尘",
                        "like": "0",
                        "like_count": "0",
                        "replied_user_id": "1",
                        "replied_nick_name": "微微笑"
                    }
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmb-comments?jmb_id=1&page=1"
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



### 加盟宝评论详情  
- 请求方式: `get`
- 请求地址: `jmb-comments/1`
- 请求参数:  
1是评论的id

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": "3",
                "jmb_id": "1",
                "user_id": "1",
                "content": "还不错",
                "pid": "0",
                "reply_pid": "0",
                "like_num": "0",
                "create_time": "2020-02-04 16:57:35",
                "update_time": null,
                "nick_name": "微微笑",
                "user_name": "微微笑",
                "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/76776565.jpg",
                "time_before": "1小时前",
                "like": "0",
                "like_count": "0",
                "child": [
                    {
                        "id": "4",
                        "jmb_id": "1",
                        "user_id": "2",
                        "content": "还不错",
                        "pid": "3",
                        "reply_pid": "3",
                        "like_num": "1",
                        "create_time": "2020-02-04 16:59:47",
                        "update_time": null,
                        "time_before": "1小时前",
                        "avatar_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/50939351.jpg",
                        "nick_name": "陌南尘",
                        "like": "0",
                        "like_count": "0",
                        "replied_user_id": "1",
                        "replied_nick_name": "微微笑"
                    }
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmb-comments/3?page=1"
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



### 加盟宝评论点赞  
- 请求方式: `post`
- 请求地址: `jmb-comment/click-like`
- 请求参数:  
```json
{
	"id": 1   评论的id
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "添加成功",
    "info": {
        "active": 1
    }
}
1 切换成已点赞的状态
```



### 加盟宝投资金额搜索  
- 请求方式: `get`
- 请求地址: `jmbs?est_init_investment=10-25万`
- 请求参数:  

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
                "apply_num": "11115",
                "est_init_investment": "10-25万",
                "image_url": "https://www.baidu.com",
                "category_name": "餐饮",
                "brand_year": "6"
            },
            {
                "name": "和府捞面",
                "direct_store_num": "121234",
                "apply_num": "11116",
                "est_init_investment": "10-25万",
                "image_url": "https://www.baidu.com",
                "category_name": "餐饮",
                "brand_year": "6"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmbs?est_init_investment=10-25%E4%B8%87&page=1"
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



### 获取加盟方式  
- 请求方式: `get`
- 请求地址: `jmb-detail/get?id=1`
- 请求参数:  
id 加盟宝id  
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "is_vip": true,
        "origin_price": "33.00",
        "vip_price": "22.00",
        "period": "永久"
    }
}
```



### 我的加盟  
- 请求方式: `get`
- 请求地址: `jmb-user/get-my`
- 请求参数:  

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "jmb_id": "1",
                "image_url": "https://www.baidu.com",
                "name": "和府捞面",
                "est_init_investment": "10-25万",
                "period": "永久",
                "contact_way": "110"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_api.com/jmb-user/get-my?page=1"
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
