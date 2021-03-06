## **用户端api**
<a href="./#用户端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [短信](./#短信)  
    - [无忧米短信](./#无忧米短信)
- [商城](./#商城)  
    - [商品列表](./#商品列表)   
    - [商品分类](./#商品分类)
    - [商品详情](./#商品详情)
    - [商品banner](./#商品banner)
- [订单](./#订单)  
    - [订单生成](./#订单生成)   
    - [订单列表](./#订单列表)   
    - [订单详情](./#订单详情)   
    - [订单取消](./#订单取消)
    - [确认收货](./#确认收货)    
    - [个人地址](./#个人地址)
    - [个人地址添加](./#个人地址添加)
    - [个人地址编辑](./#个人地址编辑)
    - [个人地址删除](./#个人地址删除)
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



## 短信  
### 无忧米短信  
- 请求方式: `post`
- 请求地址: `user/wuyoumi-sms`
- 请求参数:
```json
{
    "mobile": "18964590201"
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success"
}
```

## 商城  
### 商品列表  
- 请求方式: `get`
- 请求地址: `goods`
- 请求参数:
```json
is_seckill=1 代表是秒杀产品
is_recommend=1 代表是推荐产品
type=xxx  分类id
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "6",
            "type_name": "美妆",
            "type_id": "1",
            "name": "好看的衣服1",
            "image": "https://www.baidu.com",
            "price_now": "1.00",
            "price_origin": "3.00",
            "specification": "大号",
            "deliver_addr": "北京",
            "sold_num": "55",
            "is_seckill": "0",
            "dis_count": "3.3"
        },
        {
            "id": "5",
            "type_name": "男装",
            "type_id": "5",
            "name": "好看的衣服1",
            "image": "https://www.baidu.com",
            "price_now": "30.00",
            "price_origin": "60.00",
            "specification": "大号",
            "deliver_addr": "北京",
            "sold_num": "55",
            "is_seckill": "0",
            "dis_count": "5"
        },
        {
            "id": "4",
            "type_name": "鞋履",
            "type_id": "4",
            "name": "好看的衣服1",
            "image": "https://www.baidu.com",
            "price_now": "30.00",
            "price_origin": "60.00",
            "specification": "大号",
            "deliver_addr": "北京",
            "sold_num": "55",
            "is_seckill": "1",
            "dis_count": "5"
        }
    ]
}
```
### 商品分类  
- 请求方式: `get`
- 请求地址: `good/get-type`
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "1",
            "name": "美妆"
        },
        {
            "id": "2",
            "name": "女装"
        },
        {
            "id": "3",
            "name": "配饰"
        },
        {
            "id": "4",
            "name": "鞋履"
        },
        {
            "id": "5",
            "name": "男装"
        }
    ]
}
```
### 商品详情  
- 请求方式: `get`
- 请求地址: `goods/1`
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "1",
            "type_name": "美妆",
            "type_id": "1",
            "name": "好看的衣服1",
            "image": "https://www.baidu.com",
            "price_now": "30.00",
            "price_origin": "60.00",
            "specification": "大号",
            "deliver_addr": "北京",
            "sold_num": "55",
            "is_recommand": "0",
            "is_seckill": "0",
            "free_mail": "0",
            "free_tax": "0",
            "dis_count": "5"
        }
    ]
}
free_mail 1是包邮，free_tax1是免税，dis_count 5折，
```



### 商品banner  
- 请求方式: `get`
- 请求地址: `good/get-banner`
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "2",
            "image": "https://www.baidu.com"
        },
        {
            "id": "5",
            "image": "https://www.baidu.com"
        },
        {
            "id": "6",
            "image": "https://www.baidu.com"
        }
    ]
}
```




## 订单  
### 订单生成  
- 请求方式: `post`
- 请求地址: `good/post-order`
- 请求参数:
```json
{
	"goods_id": 1,
	"user_name": "fyx",
	"mobile": "18964590201",
	"receive_addr": "上海市浦东新区张杨路707号"
}
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": {
        "gatewayUrl": "https://openapi.alipay.com/gateway.do",
        "appId": null,
        "rsaPrivateKey": null,
        "format": "json",
        "charset": "UTF-8",
        "signType": "RSA2",
        "alipayrsaPublicKey": null,
        "notifyUrl": "http://47.103.61.179:8074/goods/async-notify",
        "bizcontent": "{\"subject\": \"好看的衣服2222\",\"out_trade_no\": \"2020011357991025\",\"total_amount\": \"30.00\",\"product_code\":\"QUICK_MSECURITY_PAY\"}"
    }
}
```

### 订单列表  
- 请求方式: `get`
- 请求地址: `good/get-order-list?status=1`
- 请求参数:
status
1已提交，2已付款，3已发货，4已收货,7已完成
```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "name": "好看的衣服2222",
            "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/banner/images2019-08-19/iBjRITW80HxbJ0J-UX769P0jsmbBHxj5.png",
            "specification": "大号",
            "price": "30.00",
            "id": "28",
            "order_sign": "2020011557101569",
            "status": "1",
            "user_name": "fyx",
            "mobile": "18964590201",
            "receive_addr": "上海市浦东新区张杨路707号",
            "goods_specification": "大号",
            "goods_service": "七天无理由退换",
            "goods_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/banner/images2019-08-19/iBjRITW80HxbJ0J-UX769P0jsmbBHxj5.png",
            "subject": "好看的衣服2222",
            "total_amount": "30.00",
            "order_detail": "alipay_sdk=alipay-sdk-php-easyalipay-20190926&app_id=2021001107603787&biz_content=%7B%22subject%22%3A+%22%E5%A5%BD%E7%9C%8B%E7%9A%84%E8%A1%A3%E6%9C%8D2222%22%2C%22out_trade_no%22%3A+%222020011557101569%22%2C%22total_amount%22%3A+%2230.00%22%2C%22product_code%22%3A%22QUICK_MSECURITY_PAY%22%7D&charset=UTF-8&format=json&method=alipay.trade.app.pay&notify_url=https%3A%2F%2Fapi.5youfenqi.com%2Fgood%2Fasync-notify&sign_type=RSA2&timestamp=2020-01-15+16%3A05%3A13&version=1.0&sign=A75NFAKY7DyQw5yZXAg7bjbO7Lk5Wykq8tynTaMNFBMy9%2BsO329wRRECso6jxcrmJFFn2P3gBepxrS%2BKELNQLCO%2FXCf9u%2FibmOnReANp7YvNBvQFiJh2dHcoZxZyap%2BEOMytvhzrQsm7xQvMYqLOSjE4B5UqdEBz%2FThJBKn2GHpJYoaR%2BcBDJ%2FNZqAWfggumDL95Al041u9YI8tfm2PTGK4rrpAx5Nkgf7EBLI%2FzH9BzhaXASlXiLVmDLtXSoqv08SETJDFM%2BmUhBCzjgm%2BKJeKpp37ay1wNgAK2Yeg%2BtsgG9dyP3uskdXEvEsTOS4PI8QyWKd3AZAldJgdoEAIi6A%3D%3D"
        }
    ]
}
```

### 订单详情  
- 请求方式: `get`
- 请求地址: `good/get-order-detail?order_sign=2020010848484897`
- 请求参数:

```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": "1",
            "type_name": "女装",
            "type_id": "2",
            "name": "好看的衣服2222",
            "image": "https://xijin.oss-cn-shanghai.aliyuncs.com/banner/images2019-08-19/iBjRITW80HxbJ0J-UX769P0jsmbBHxj5.png",
            "price_now": "30.00",
            "price_origin": "60.00",
            "specification": "大号",
            "detail_url": "https://www.baidu.com",
            "deliver_addr": "北京",
            "sold_num": "55",
            "is_seckill": "1",
            "is_recommand": "0",
            "free_mail": "0",
            "free_tax": "0",
            "receive_addr": "上海市浦东新区张杨路707号",
            "mobile": "18964590201",
            "user_name": "fyx",
            "dis_count": "5",
            "state": "3",
            "logistics": [
                {
                    "time": "2019-11-27 18:55:27",
                    "ftime": "2019-11-27 18:55:27",
                    "context": "[上海青浦白鹤营业点]已签收,感谢使用顺丰,期待再次为您服务（主单总件数：1件）"
                },
                {
                    "time": "2019-11-27 18:34:51",
                    "ftime": "2019-11-27 18:34:51",
                    "context": "[白鹤速运营业点]快件交给,正在派送途中（联系电话：,顺丰已开启“安全呼叫”保护您的电话隐私,请放心接听！）"
                },
                {
                    "time": "2019-11-27 18:01:14",
                    "ftime": "2019-11-27 18:01:14",
                    "context": "[白鹤速运营业点]快件到达 【上海青浦白鹤营业点】"
                },
                {
                    "time": "2019-11-27 16:20:57",
                    "ftime": "2019-11-27 16:20:57",
                    "context": "[上海虹桥同城集散点]快件已发车"
                },
                {
                    "time": "2019-11-27 16:20:42",
                    "ftime": "2019-11-27 16:20:42",
                    "context": "快件在【上海虹桥同城集散点】已装车,准备发往下一站"
                },
                {
                    "time": "2019-11-27 15:38:24",
                    "ftime": "2019-11-27 15:38:24",
                    "context": "快件到达 【上海虹桥同城集散点】"
                },
                {
                    "time": "2019-11-27 14:07:26",
                    "ftime": "2019-11-27 14:07:26",
                    "context": "[上海卢湾同城集散点]快件已发车"
                },
                {
                    "time": "2019-11-27 13:42:10",
                    "ftime": "2019-11-27 13:42:10",
                    "context": "快件在【上海卢湾同城集散点】已装车,准备发往下一站"
                },
                {
                    "time": "2019-11-27 13:42:10",
                    "ftime": "2019-11-27 13:42:10",
                    "context": "快件到达 【上海卢湾同城集散点】"
                },
                {
                    "time": "2019-11-27 13:00:37",
                    "ftime": "2019-11-27 13:00:37",
                    "context": "[陆家嘴速运营业点]快件已发车"
                },
                {
                    "time": "2019-11-27 13:00:24",
                    "ftime": "2019-11-27 13:00:24",
                    "context": "[陆家嘴速运营业点]快件在【上海浦东陆家嘴营业点】已装车,准备发往 【上海卢湾同城集散点】"
                },
                {
                    "time": "2019-11-27 10:54:37",
                    "ftime": "2019-11-27 10:54:37",
                    "context": "[陆家嘴速运营业点]顺丰速运 已收取快件"
                }
            ]
        }
    ]
}
receive_addr 地址信息
```


### 订单取消  
- 请求方式: `post`
- 请求地址: `good/post-update-order`
- 请求参数:
```json
{
   "order_sign": "2020010898579710",
   "status": "5"
}
status 是5，写死
```

```
- 响应内容:  
```json
取消之后显示订单已关闭
{
    "code": 1,
    "message": "success",
    "info": ""
}
```

### 确认收货  
- 请求方式: `post`
- 请求地址: `good/post-update-order`
- 请求参数:
```json
{
   "order_sign": "2020010898579710",
   "status": "4"
}
status 是4，写死
```

```
- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": ""
}
```


### 个人地址  
- 请求方式: `get`
- 请求地址: `good/get-addr`
- 请求参数:

- 响应内容:  
```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
		"id":1,
		"addr": "上海。。",
		"province":"11",
		"city":"xxx",
		"district":"xxxx"
        },
        {
		"id":1,
		"addr": "上海。。",
		"province":"11",
		"city":"xxx",
		"district":"xxxx"
        }
    ]
}
```

### 个人地址添加  
- 请求方式: `post`
- 请求地址: `good/add-addr`
- 请求参数:
```json
{
	"addr": "上海。。",
	"province":"11",
	"city":"xxx",
	"district":"xxxx"
}
```
- 响应内容:  
```json

```


### 个人地址编辑  
- 请求方式: `post`
- 请求地址: `good/edit-addr`
- 请求参数:
```json
{
	"id":1,
	"addr": "上海。。",
	"province":"11",
	"city":"xxx",
	"district":"xxxx"
}
```
- 响应内容:  
```json

```

### 个人地址删除  
- 请求方式: `post`
- 请求地址: `good/del-addr`
- 请求参数:
```json
{
	"id":1
}
```
- 响应内容:  
```json

```
