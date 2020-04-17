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
- 请求地址: {host}`order-list`

- 响应内容:  
status   200：审批中； 300：审批通过； 400：审批拒绝； 500：额度冻结  
maxLoanAmt   审批额度  
approveTime   审核日期  
face_flow_id   活体校验流水号  
withdraw_id   提现订单号  

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


