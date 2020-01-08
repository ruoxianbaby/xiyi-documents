## **用户端api**
<a href="./#用户端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [商城](./#商城)  
    - [商品列表](./#商品列表)   
    - [商品分类](./#商品分类)
    - [商品详情](./#商品详情)
    - [商品banner](./#商品banner)
- [订单](./#订单)  
    - [订单生成](./#订单生成)   
  
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
        "user_id": 97,
        "goods_id": 1,
        "user_name": "fyx",
        "mobile": "18964590201",
        "receive_addr": "上海市浦东新区张杨路707号",
        "status": 1,
        "order_sign": "2020010855574857",
        "create_time": "2020-01-08 15:29:59",
        "id": 5
    }
}
```
