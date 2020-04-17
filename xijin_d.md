### **Client_api**

<a href="./#client_api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>

### 测试主机host: 47.103.61.179:1022/  
- [超即花](./#超即花)  
    - [审核记录](./#审核记录)  
    
### 全局header  

key |  vaule
----- | --------
Accept | application/json
Content-Type | application/json

需要验证的接口加上:  
  
key |  vaule
----- | --------
Authorization | Bearer ***access_token***  



## 超即花

### 审核记录
- 请求方式: `get`
- 请求地址: {host}`cjh-open-api/order-list`

- 响应内容:  
status   200：审批中； 300：审批通过； 400：审批拒绝； 500：额度冻结  
maxLoanAmt&nbsp;&nbsp;&nbsp;审批额度  
approveTime&nbsp;&nbsp;&nbsp;审核日期  
face_flow_id&nbsp;&nbsp;&nbsp;活体校验流水号  
withdraw_id&nbsp;&nbsp;&nbsp;提现订单号  

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "id": "241",
            "no": "202004151553566272868616",
            "u_id": "1",
            "status": "300",
            "audit_data": {
                "status": "300",
                "amtRange": 100,
                "maxLoanAmt": 50000,
                "minLoanAmt": 1000,
                "amountLimit": {
                    "totalAmount": 50000,
                    "surplusAmount": 50000
                },
                "approveTime": 1586758320000,
                "termOptions": [
                    {
                        "name": "现金贷-1期-超即花",
                        "term": 1,
                        "termId": 2038
                    },
                    {
                        "name": "现金贷-3期-超即花",
                        "term": 3,
                        "termId": 2044
                    },
                    {
                        "name": "现金贷-6期-超即花",
                        "term": 6,
                        "termId": 2047
                    },
                    {
                        "name": "1",
                        "term": 2,
                        "termId": 2168
                    }
                ]
            },
            "face_flow_id": "",
            "withdraw_id": "",
            "create_time": "2020-04-15 15:53:56",
            "update_time": "2020-04-15 15:57:35"
        },
        {
            "id": "240",
            "no": "202004151542362667520532",
            "u_id": "1",
            "status": "300",
            "audit_data": {
                "status": "300",
                "channel": "SUISHOU01",
                "orderNo": "202004151542362667520532",
                "amtRange": 100,
                "isCustom": 0,
                "maxLoanAmt": 50000,
                "minLoanAmt": 1000,
                "amountLimit": {
                    "totalAmount": 50000,
                    "surplusAmount": 50000
                },
                "approveTime": 1586937237965,
                "termOptions": [
                    {
                        "name": "现金贷-1期-超即花",
                        "term": 1,
                        "termId": 2038
                    },
                    {
                        "name": "现金贷-3期-超即花",
                        "term": 3,
                        "termId": 2044
                    },
                    {
                        "name": "现金贷-6期-超即花",
                        "term": 6,
                        "termId": 2047
                    },
                    {
                        "name": "1",
                        "term": 2,
                        "termId": 2168
                    }
                ]
            },
            "face_flow_id": "",
            "withdraw_id": "",
            "create_time": "2020-04-15 15:42:36",
            "update_time": "2020-04-15 15:53:58"
        }
    ]
}
```

### 银行列表
- 请求方式: `get`
- 请求地址: {host}`/bank-list`

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "bankCode": "BOB",
            "bankName": "北京银行",
            "icon": "http://download.geexfinance.com/bankList-V1/BOB@3x.png"
        },
        {
            "bankCode": "CBHB",
            "bankName": "渤海银行",
            "icon": "http://download.geexfinance.com/bankList-V1/CBHB@3x.png"
        }
    ]
}
```

### 银行列表
- 请求方式: `get`
- 请求地址: {host}`/cjh-open-api/bank-list`

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "bankCode": "BOB",
            "bankName": "北京银行",
            "icon": "http://download.geexfinance.com/bankList-V1/BOB@3x.png"
        },
        {
            "bankCode": "CBHB",
            "bankName": "渤海银行",
            "icon": "http://download.geexfinance.com/bankList-V1/CBHB@3x.png"
        }
    ]
}
```

### 银行卡列表
- 请求方式: `get`
- 请求地址: {host}`/cjh-open-api/bank-card-list`

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "bankCode": "ABC",
            "bankName": "农业银行",
            "cardNo": "6228481099305925274",
            "channel": "SUISHOU01",
            "defaultFlag": true,
            "idNo": "123456196108041236",
            "name": "奧巴哈",
            "reserveMobile": "13701874183",
            "uid": "1b7d7a937d3811eab7fab7e6d7245602"
        }
    ]
}
```

### 银行卡绑卡
- 请求方式: `post`
- 请求地址: {host}`/cjh-open-api/bank-card-bind`

- 请求内容:  

```json
{
    orderNo:202004151032496186912628
    idNo:123456196108041236
    name:奧巴哈
    cardNo:6228481099305925274
    bankCode:ABC
    bankName:农业银行
    reserveMobile:13701874183
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "绑卡成功",
    "info": ""
}
```
or
```json
{
    "code": 1,
    "message": "验证码发送成功",
    "info": ""
}
```

### 银行卡验证码绑卡
- 请求方式: `post`
- 请求地址: {host}`/cjh-open-api/bank-card-bind-captcha`

- 请求内容:  

```json
{
    orderNo:202004151032496186912628
    idNo:123456196108041236
    name:奧巴哈
    cardNo:6228481099305925274
    bankCode:ABC
    bankName:农业银行
    reserveMobile:13701874183
    verifyCode:1234
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "绑卡成功",
    "info": ""
}
```

### 贷款试算
- 请求方式: `get`
- 请求地址: {host}`/cjh-open-api/loan-calculate`

- 请求内容:  
注:&nbsp;
```json
{
    amount:1000
    period:2
    orderNo:202004151553566272868616
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": {
        "actualAmount": 1000,
        "payAmount": 1036,
        "payFee": 36,
        "remark": "本金1000.00元，利息36.00元",
        "repayPlan": [
            {
                "payAmount": 518,
                "payCorpus": 500,
                "payDate": 1596643200000,
                "payFee": 18,
                "serviceCharge": 0,
                "tenor": 1
            },
            {
                "payAmount": 518,
                "payCorpus": 500,
                "payDate": 1599321600000,
                "payFee": 18,
                "serviceCharge": 0,
                "tenor": 2
            }
        ],
        "serviceFee": 0
    }
}
```