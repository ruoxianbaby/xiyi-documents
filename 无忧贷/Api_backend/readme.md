## **服务端api**
<a href="./#服务端api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>
- [物流模块](./#物流模块)  
    - [物流添加](./#物流添加)  
    - [物流公司信息](./#物流公司信息)  
    - [待发货商品列表](./#待发货商品列表)     
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

## 物流模块
### 物流添加
- 也就是物流发货
- 请求方式: `post`
- 请求地址: {host}`goods-order/deliver-good`
- 请求参数:  

```json
{
    "com": "yuantong",    --- goods-order/get-deliver-num 的company_num字段
    "num": "kuaiDIdAnHao",
    "phone": "23214234234",
    "goods_order_id": 1   --- goods-order/get-undeliver-goods
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

### 物流公司信息
- 请求方式: `get`
- 请求地址: {host}`goods-order/get-deliver-num`
- 请求参数:  

```json

```  
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": [
        {
            "id": 1,
            "company_name": "韵达快递",
            "company_num": "yunda"
        },
        {
            "id": 2,
            "company_name": "中通快递",
            "company_num": "zhongtong"
        },
        {
            "id": 3,
            "company_name": "顺丰速运",
            "company_num": "shunfeng"
        }
    ]
}
```

### 待发货商品列表
- 请求方式: `get`
- 请求地址: {host}`goods-order/get-undeliver-goods`
- 请求参数:  

```json

```  
- 响应内容:  

```json
只需要拿goods_id
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 2,
                "order_sign": "2020011357991025",
                "goods_id": 1,
                "goods_name": "好看的衣服2222",
                "goods_specification": "大号",
                "goods_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/banner/images2019-08-19/iBjRITW80HxbJ0J-UX769P0jsmbBHxj5.png",
                "goods_price": "30.00",
                "goods_service": "七天无理由退换",
                "user_id": 97,
                "user_name": "fyx",
                "mobile": "18964590201",
                "receive_addr": "上海市浦东新区张杨路707号",
                "status": 2,
                "bizcontent": null,
                "create_time": "2020-01-13 17:23:53",
                "update_time": null,
                "type_name": 122
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_sshua_backend.com/goods-order/get-undeliver-goods?page=1"
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
