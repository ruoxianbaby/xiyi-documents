## **后台api**
<a href="./#后台api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [加盟宝](./#加盟宝)
    - [banner图一套restful](./#banner图一套restful)  
    - [获得广告图片](./#获得广告图片) 
    - [广告图片修改](./#广告图片修改)
    - [热门专区一套restful](./#热门专区一套restful)
    - [加盟宝一套restful](./#加盟宝一套restful)
    - [一级分类一套restful](./#一级分类一套restful)
    - [二级分类一套restful](./#二级分类一套restful)
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




### 加盟宝一套restful  
- 请求方式: `post`
- 请求地址: `jmbs`
- 请求参数:  
```json
{
    "name": "和府捞面",
    "jmb_category_id": 5,
    "brand_name": "品牌123",
    "desc": "描述",
    "direct_store_num": 121234,
    "join_store_num": 222,
    "apply_num": 11121,
    "buy_num": 0,
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
    "is_hot_join": 1,
    "is_hot_recommend": 1,
    "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg",
    "info": "富文本内容",
    "status": 1,
    "create_time": "2020-02-03 15:11:27",
    "update_time": null,
    "type": "0",
    "period": "0",
    "origin_price": "33.00",
    "vip_price": "22.00",
    "contact_mobile": "18964590211",
    "contact_person": "lixiaojie",
    "contact_person_job": "经理"
}
```

 * @property string $name 加盟宝名称
 * @property int $jmb_category_id 分类id
 * @property string $brand_name 品牌名称
 * @property string $desc 描述
 * @property int $direct_store_num 直营店数量
 * @property int $join_store_num 加盟店数量
 * @property int $apply_num 申请加盟数量
 * @property int $buy_num 有多少个人购买了联系方式
 * @property string $main_project 主营项目
 * @property string $register_time 品牌注册时间
 * @property string $location 公司所在地
 * @property string $est_init_investment 预估初始投资
 * @property string $est_customer_unit_price 预估客单价
 * @property string $est_customer_daily_flow 预估日客流量
 * @property string $est_mothly_sale 预估月销售额
 * @property string $est_gross_profit 预估毛利润
 * @property string $est_payback_period 预估回报周期
 * @property string $inital_fee 初期预计投入
 * @property string $join_fee 加盟费
 * @property string $deposit_fee 保证金
 * @property string $device_fee 设备费用
 * @property string $other_fee 其他费用
 * @property int $is_hot_join 热门分类中的名牌加盟 1是 0否
 * @property int $is_hot_recommend 是否是首页热门推荐 1是 0否
 * @property string $image_url 背景图片
 * @property string $info 富文本内容
 * @property int $status 状态1启用 0禁用
 * @property int $type 类型：0电话联系
 * @property string $origin_price 非vip价
 * @property string $vip_price vip价
 * @property int $period 有效期 0永久
 * @property string $contact_mobile 联系电话
 * @property string $contact_person 联系人昵称
 * @property string $contact_person_job 联系人职位
```


- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": ""
}
```




### 一级分类一套restful  
- 请求方式: `get`
- 请求地址: `jmb-cates`
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
                "name": "餐饮",
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
            },
            {
                "id": 2,
                "name": "教育",
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
            },
            {
                "id": 3,
                "name": "酒店",
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
            },
            {
                "id": 4,
                "name": "早教",
                "image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_service.com/jmb-cates?page=1"
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




### 二级分类一套restful  
- 请求方式: `post`
- 请求地址: `jmb-sub-cates`
- 请求参数:  
```json
{
	"pid": 1,  父级别分类的id
	"name": "2级分类",
	"image_url": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/timg%20%285%29.jpg"
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": ""
}
```
