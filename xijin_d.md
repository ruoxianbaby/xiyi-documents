### **Client_api**

### 测试主机host: 47.103.61.179:1022/  
- [超即花](./xijin_d.md/#超即花)  
    - [审核记录去还款借还记录](./xijin_d.md/#审核记录去还款借还记录)  
    - [银行列表](./xijin_d.md/#银行列表)  
    - [银行卡列表](./xijin_d.md/#银行卡列表)  
    - [银行卡绑卡](./xijin_d.md/#银行卡绑卡)  
    - [银行卡验证码绑卡](./xijin_d.md/#银行卡验证码绑卡)  
    - [贷款试算](./xijin_d.md/#贷款试算)  
    - [合同预览](./xijin_d.md/#合同预览)  
    - [活体校验](./xijin_d.md/#活体校验)  
    - [提现申请](./xijin_d.md/#提现申请)  
    - [用户信息](./xijin_d.md/#用户信息)  
    - [还款计划](./xijin_d.md/#还款计划)  

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

### 审核记录去还款借还记录
- 请求方式: `get`
- 请求地址: {host}`cjh-open-api/order-list?type=`  
type　0：审核记录；１：去还款；２：借还记录；

- 响应内容:  
order_status　200：审批中； 300：审批通过； 400：审批拒绝； 500：额度冻结；4001提现审批中； 4002提现审批通过； 4003提现审批拒绝； 4009贷款取消； 4101放款成功； 4102放款失败； 4201还款中； 4202已逾期； 4203贷款结清  
maxLoanAmt　最高贷款金额  
minLoanAmt　最小贷款金额  
amtRange　最大审批金额和最小审批金额间的最小变更金额  
approveTime　审核日期  
face_flow_id　活体校验流水号  
withdraw_id　提现订单号  
loanAmount　放款金额  
remainTime　剩余时间  

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "id": "263",
            "no": "202004211400163844171940",
            "u_id": "4",
            "status": "300",
            "audit_data": {
                "status": "300",
                "channel": "SUISHOU01",
                "orderNo": "202004211400163844171940",
                "amtRange": 100,
                "isCustom": 0,
                "maxLoanAmt": 50000,
                "minLoanAmt": 1000,
                "amountLimit": {
                    "totalAmount": 50000,
                    "surplusAmount": 50000
                },
                "approveTime": "2020-04-21",
                "termOptions": [
                    {
                        "name": "现金贷-12期  超即花",
                        "term": 12,
                        "termId": 1333
                    },
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
                ],
                "remainTime": "6天"
            },
            "loan_status": "4002",
            "loan_data": {
                "orderNo": "202004211400163844171940",
                "loanAmount": 1000,
                "orderStatus": "4002",
                "userMonthFee": 1.6
            },
            "face_flow_id": "76eca81b-8398-11ea-9117-8534739079ee",
            "withdraw_id": "2446255427175216",
            "create_time": "2020-04-21 14:00:16",
            "update_time": "2020-04-21 14:23:45",
            "order_status": "4002",
            "product_name": "test-cjh",
            "image": "https://xijin-loan.oss-cn-shanghai.aliyuncs.com/product/images/%E5%B0%8F%E8%8A%B1_EktrkEOSTRVzBoX1zhINiKPzLq9CAN4c_RS8dSHY5Yr4Y9-DYTZlnLCKqUuMxBf3X.jpg",
            "order_status_msg": "审批通过",
            "approveTime": "2020-04-22"
        }
    ]
}
```

### 银行列表
- 请求方式: `GET`
- 请求地址: {host}`/cjh-open-api/bank-list`
测试账号　ICBC  ，6212262406000281813 ； ABC  ，6228481099305925274； 

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": [
        {
            "bankCode": "ICBC",
            "bankName": "工商银行",
            "icon": "http://download.geexfinance.com/bankList-V1/ICBC@3x.png"
        },
        {
            "bankCode": "ABC",
            "bankName": "农业银行",
            "icon": "http://download.geexfinance.com/bankList-V1/ABC@3x.png"
        }
    ]
}
```

### 银行卡列表
- 请求方式: `GET`
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
            "idNo": "310107199104053435",
            "name": "沈黎昂",
            "reserveMobile": "13701874180",
            "uid": "60c1f119839511ea9117df7a35ff2bf3"
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
    "orderNo":202004151032496186912628,
    "idNo":123456196108041236,
    "name":"奧巴哈",
    "cardNo":6228481099305925274,
    "bankCode":"ABC",
    "bankName":"农业银行",
    "reserveMobile":13701874183
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "绑卡成功",
    "info": {
        "status": "3001"
    }
}
```
or
```json
{
    "code": 1,
    "message": "验证码发送成功",
    "info": {
        "status": "3003"
    }
}
```

### 银行卡验证码绑卡
- 请求方式: `post`
- 请求地址: {host}`/cjh-open-api/bank-card-bind-captcha`

- 请求内容:  

```json
{
    "orderNo":202004151032496186912628,
    "idNo":123456196108041236,
    "name":"奧巴哈",
    "cardNo":6228481099305925274,
    "bankCode":"ABC",
    "bankName":"农业银行",
    "reserveMobile":13701874183,
    "verifyCode":1234
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
- 请求方式: `POST`
- 请求地址: {host}`/cjh-open-api/loan-calculate`

- 请求内容:  
注:&nbsp;&nbsp;&nbsp;period&nbsp;&nbsp;&nbsp;取决于审核列表的&nbsp;&nbsp;&nbsp;termOptions
```json
{
    "amount":1000,
    "period":2,
    "orderNo":202004151553566272868616
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": {
        "actualAmount": 1000,
        "payAmount": 1037.52,
        "payFee": 47.52,
        "remark": "本金1000.00元，利息47.52元",
        "repayPlan": [
            {
                "payAmount": 345.84,
                "payCorpus": 330,
                "payDate": 1596643200000,
                "payFee": 15.84,
                "serviceCharge": 0,
                "tenor": 1
            },
            {
                "payAmount": 345.84,
                "payCorpus": 330,
                "payDate": 1599321600000,
                "payFee": 15.84,
                "serviceCharge": 0,
                "tenor": 2
            },
            {
                "payAmount": 345.84,
                "payCorpus": 330,
                "payDate": 1601913600000,
                "payFee": 15.84,
                "serviceCharge": 0,
                "tenor": 3
            }
        ],
        "serviceFee": 0
    }
}
```

### 合同预览
- 请求方式: `POST`
- 请求地址: {host}`/cjh-open-api/contract-show`

- 请求内容:  
orderNo&nbsp;&nbsp;&nbsp;渠道方订单号  
contractNo&nbsp;&nbsp;&nbsp;合同编号&nbsp;&nbsp;&nbsp;1委托代扣协议&nbsp;&nbsp;&nbsp;2居间服务协议，&nbsp;&nbsp;&nbsp;3借款合同，&nbsp;&nbsp;&nbsp;4数据查询授权书

- 响应内容:  

```json
{
    "code": 1,
    "message": "Success",
    "info": {
        "contractUrl": "https://beta.geexfinance.com/geexweixinb/views/app/chaojihua/commission_withholding.html?cName=%E5%A5%A7%E5%B7%B4%E5%93%88&cIdno=123456196108041236"
    }
}
```

### 活体校验
- 请求方式: `POST`
- 请求地址: {host}`/cjh-open-api/user-verify`

- 请求内容:  
```json
{
    "orderNo":"202004151032496186912628",
    "image1": "data:image/jpg;base64,/9j/4AAQSkZJRgABAQEASABIAAD/4QBsRXhpZgAASUkqAAgAAAADADEBAgAHAAAAMgAAABICAwACAAAAAgACAGmHBAABAAAAOgAAAAAAAABQaWNhc2EAAAMAAJAHAAQAAAAwMjIwAqAEAAEAAAD0AQAAA6AEAAEAAAAsAQAAAAAAAP/bAEMABwUFBgUEBwYFBggHBwgKEQsKCQkK................"
}
```

- 响应内容:  

```json
{
    "code": 0,
    "message": "提交成功",
    "info": ""
}
```

### 提现申请
- 请求方式: `POST`
- 请求地址: {host}`/cjh-open-api/loan-submit`

- 请求内容:  
```json
{
    "orderNo":202004151032496186912628,
    "loanAmt":1000,
    "period":3
}
```

- 响应内容:  

```json
{
    "code": 0,
    "message": "审批提现前置条件不符合",
    "info": ""
}
```

### 用户信息
- 请求方式: `GET`
- 请求地址: {host}`/cjh-open-api/user-info`  
verifiedIdName　姓名  
verifiedIdNo　身份证  

- 响应内容:  

```json
{
    "code": 1,
    "message": "SUCCESS",
    "info": {
        "name1": "联系人",
        "name2": "联系从",
        "degree": "40",
        "mobile1": "110",
        "mobile2": "120",
        "marriage": "01",
        "houseCity": "北京市",
        "relation1": "8",
        "relation2": "5",
        "companyCity": "北京市",
        "companyName": "公司名称",
        "verifiedIdNo": "310107199104053401",
        "houseCityCode": "110000",
        "houseDistrict": "东城区",
        "houseProvince": "北京市",
        "monthlyIncome": "37",
        "preCreditScore": "100",
        "verifiedIdName": "沈黎昂",
        "verifiedIdRace": "汉",
        "companyCityCode": "110000",
        "companyDistrict": "东城区",
        "companyProvince": "北京市",
        "verifiedIdGender": "男",
        "verifiedIdIssued": "上海市公安局静安分局",
        "houseDistrictCode": "110101",
        "houseProvinceCode": "110000",
        "verifiedIdAddress": "上海市静安区中华新路940号901室",
        "houseDetailAddress": "家庭详细地址",
        "verifiedIdBirthday": "19910405",
        "verifiedIdValidEnd": "20370805",
        "companyDistrictCode": "110101",
        "companyProvinceCode": "110000",
        "verifiedIdValidBegin": "20170805"
    }
}
```

### 还款计划
- 请求方式: `POST`
- 请求地址: {host}`/cjh-open-api/repay-plan-list`  
- 请求内容:  
```json
{
    "orderNo":202004151032496186912628
}
```
- 响应内容:  
loanAmount　借款金额  
orderNo　订单号  
createTime　借款日期  
allPayAmount　合计  
payedAmount　已还  
needPayAmount　待还  
repayPlan:  
allPayAmount　总金额  
isPaid　当期是否已结清  
lateFee　当期违约金  
currTenor　当前期数  

```json
{
    "code": 0,
    "message": "Success",
    "info": {
        "bankCode": "ABC",
        "bankName": "",
        "cardNo": "6228481099305925274",
        "earlyRepay": 0,
        "orderNo": "202004231024255422109743",
        "repayPlan": [
            {
                "allPaidAmount": 0,
                "allPayAmount": 349.43,
                "allPayCorpus": 330.02,
                "allPayFee": 19.41,
                "canRepayDate": 1587657600000,
                "canRepayStatus": true,
                "corpusAmt": 330.02,
                "currTenor": 1,
                "isPaid": false,
                "isPaying": false,
                "lateFee": 0,
                "overDays": 0,
                "payDate": 1589904000000,
                "payTillTime": "23:00:00",
                "payType": 3,
                "remainAmount": 349.43
            }
        ],
        "withdrawId": "2447554854052707",
        "loanAmount": "1000.00",
        "createTime": "2020-04-23",
        "needPayAmount": 1047.96,
        "allPayAmount": 1047.96,
        "payedAmount": 0
    }
}
```
