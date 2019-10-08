### **Service_api**

<a href="./#client_api" style="height:50px;width:35px;position:fixed;bottom:100px;right:0px;background:#00BCC1;opacity:0.6;color:#333;text-decoration:none;">回到顶部</a>

### 测试主机host: 47.103.61.179:1081  
- [创业邦](./#创业邦)  
    - [创业列表](./#创业列表)  
- [反馈管理](./#反馈管理)  
    - [反馈列表](./#反馈列表)  
    - [反馈删除](./#反馈删除)  
- [电台](./#电台)  
    - [电台列表](./#电台列表)  
    - [电台详情](./#电台详情)  
    - [电台新增](./#电台新增)    
    - [电台更新](./#电台更新)  
    - [时间轴列表](./#时间轴列表)     
## 创业邦

### 创业列表
- 请求方式: `get`
- 请求地址: {host}`businesses`




- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "items": [
            {
                "id": 45,
                "u_id": 121,
                "b_id": 12,
                "c_id": 440100,
                "t_id": 1,
                "area": "互联网金融",
                "description": "和别别扭扭很呵呵改改改改改计算机二级",
                "interested_nums": 0,
                "create_time": "2019-09-12 15:08:24",
                "update_time": "0000-00-00 00:00:00",
                "end_time": "2019-09-01",
                "status": 1,
                "is_del": 0,
                "is_pri": 0,
                "type_name": "求贤令",
                "city_name": "广州市",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/SgDx7sodoA28zPS3soPjWSfDmaf0mQE4.jpg",
                "pic_list": [
                    "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-12/ZFKP0ah5ZJJtyLAVi-e6E81IAag1bfTX.png",
                    "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-12/FU_cuqDRGLdls5uA9DkfFTPxXmd8-6H4.png",
                    "https://xijin.oss-cn-shanghai.aliyuncs.com/avatar/images/2019-09-12/F9D4h7YX9ro2NhQyaIHFXaGnQv4D5U2H.png"
                ]
            },
            {
                "id": 44,
                "u_id": 253,
                "b_id": 17,
                "c_id": 710000,
                "t_id": 5,
                "area": "bug",
                "description": "描述",
                "interested_nums": 0,
                "create_time": "2019-09-11 15:25:27",
                "update_time": "0000-00-00 00:00:00",
                "end_time": "2019-09-01",
                "status": 1,
                "is_del": 0,
                "is_pri": 0,
                "type_name": "其他活动",
                "city_name": "台湾省",
                "background_image": "https://xijin.oss-cn-shanghai.aliyuncs.com/bang/images2019-08-28/HXcfqf1odPn-AknIN5YcK3kD3vWLJ--4.jpg",
                "pic_list": [
                    "https://xijin-test.oss-cn-shanghai.aliyuncs.com/image/122066b0-a461-4369-ba9a-75155dd1cb3e.jpg"
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://xj.sve.org/businesses?page=1"
            },
            "next": {
                "href": "http://xj.sve.org/businesses?page=2"
            },
            "last": {
                "href": "http://xj.sve.org/businesses?page=3"
            }
        },
        "_meta": {
            "totalCount": 45,
            "pageCount": 3,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```

### 创业发布
- 请求方式: `post`
- 请求地址: {host}`businesses`
- 请求参数:  
```json
{
    "b_id": "创业背景图列表id",
    "c_id": "城市搜索列表id",
    "t_id": "创业类型列表id",
    "area": "领域",
    "end_time": "结束时间 e.g. 2019-09",
    "description": "描述",
    "pics": [ 
	"https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg",
	"https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
    ]
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "b_id": 1,
        "c_id": 1,
        "t_id": 1,
        "area": "领域",
        "end_time": "2019-09",
        "description": "描述",
        "id": 1
    }
}
```

### 创业修改
- 请求方式: `post`
- 请求地址: {host}`businesses/:id`
- 请求参数:  
```json
{
    "b_id": "创业背景图列表id",
    "c_id": "城市搜索列表id",
    "t_id": "创业类型列表id",
    "area": "领域",
    "end_time": "结束时间 e.g. 2019-09",
    "description": "描述",
    "pics": [ 
	    "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg",
	    "https://xijin.oss-cn-shanghai.aliyuncs.com/user_demo_avatar/45973393.jpg"
    ]
}
```

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "b_id": 1,
        "c_id": 1,
        "t_id": 1,
        "area": "领域",
        "end_time": "2019-09",
        "description": "描述",
        "id": 1
    }
}
```

### 创业删除
- 请求方式: `delete`
- 请求地址: {host}`businesses/:id`

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        
    }
}
```

### 创业设置私有
- 请求方式: `post`
- 请求地址: {host}`business/set-private`
- 请求参数:  
id,is_pri

- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        
    }
}
```

## 反馈管理

### 反馈列表
- 请求方式: `get`
- 请求地址: {host}`suggestions`
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
                "user_id": 1,
                "content": "反馈的内容",
                "mobile": "联系人手机 可选的",
                "email": "联系人邮箱 也是可选的",
                "create_time": "2019-09-16 10:47:04",
                "nick_name": "微微笑",
                "pics": []
            },
            {
                "id": 2,
                "user_id": 1,
                "content": "哈哈",
                "mobile": "联系人手机 可选的",
                "email": "联系人邮箱 也是可选的",
                "create_time": "2019-09-16 10:47:02",
                "nick_name": "微微笑",
                "pics": []
            },
            {
                "id": 3,
                "user_id": 1,
                "content": "反馈的内容",
                "mobile": "联系人手机 可选的",
                "email": "联系人邮箱 也是可选的",
                "create_time": "2019-09-16 10:47:00",
                "nick_name": "微微笑",
                "pics": []
            },
            {
                "id": 5,
                "user_id": 1,
                "content": "反馈的内容",
                "mobile": "联系人手机 可选的",
                "email": "联系人邮箱 也是可选的",
                "create_time": "2019-09-03 13:54:11",
                "nick_name": "微微笑",
                "pics": []
            },
            {
                "id": 6,
                "user_id": 1,
                "content": "反馈的内容",
                "mobile": "联系人手机 可选的",
                "email": "联系人邮箱 也是可选的",
                "create_time": "2019-09-03 13:55:03",
                "nick_name": "微微笑",
                "pics": [
                    {
                        "id": "6",
                        "img_url": "https://www.baidu.com"
                    },
                    {
                        "id": "7",
                        "img_url": "https://www.jd.com"
                    }
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_service.com/suggestions?page=1"
            }
        },
        "_meta": {
            "totalCount": 5,
            "pageCount": 1,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```

### 反馈删除
- 请求方式: `delete`
- 请求地址: {host}`suggestions/3`
- 请求参数:  3是反馈的id

- 响应内容:  

```json
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```

## 电台

### 电台列表
- 请求方式: `get`
- 请求地址: {host}`radios`
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
                "radio_url": "https://alioss.gcores.com/uploads/audio/e7486ee5-d5c8-4621-ba8a-752bf762f8bc.mp3",
                "type": 1,
                "origin": "来源1",
                "title": "标题1",
                "desc": "描述",
                "preview_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/05b93d90b5b94b71a5dd8020587f33c6.jpeg",
                "comment_num": 4,
                "like_num": 3,
                "create_time": "2019-09-26 10:45:27",
                "update_time": "2019-09-26 10:45:30",
                "creater": 25,
                "admin_id": 0,
                "status": 1
            },
            {
                "id": 2,
                "radio_url": "https://alioss.gcores.com/uploads/audio/52d73fbd-6add-4c3c-b922-4ef3347fc33d.mp3",
                "type": 1,
                "origin": "来源2",
                "title": "标题2",
                "desc": "描述",
                "preview_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/%E9%A6%96%E9%A1%B51.png",
                "comment_num": 14,
                "like_num": 1,
                "create_time": "2019-09-26 10:45:27",
                "update_time": "2019-09-26 10:45:30",
                "creater": 25,
                "admin_id": 0,
                "status": 1
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_service.com/radios?page=1"
            },
            "next": {
                "href": "http://my_xijin_service.com/radios?page=2"
            },
            "last": {
                "href": "http://my_xijin_service.com/radios?page=2"
            }
        },
        "_meta": {
            "totalCount": 22,
            "pageCount": 2,
            "currentPage": 1,
            "perPage": 20
        }
    }
}
```


### 电台详情
- 请求方式: `get`
- 请求地址: {host}`radios/1?expand=content,label_id_list`
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
                "radio_url": "https://alioss.gcores.com/uploads/audio/e7486ee5-d5c8-4621-ba8a-752bf762f8bc.mp3",
                "type": 1,
                "origin": "来源1",
                "title": "标题1",
                "desc": "描述",
                "preview_image": "https://sshua.oss-cn-shanghai.aliyuncs.com/product/images/05b93d90b5b94b71a5dd8020587f33c6.jpeg",
                "comment_num": 4,
                "like_num": 3,
                "create_time": "2019-09-26 10:45:27",
                "update_time": "2019-09-26 10:45:30",
                "creater": 25,
                "admin_id": 0,
                "status": 1,
                "content": "内容",
                "label_id_list": [
                    "标签1",
                    "标签2",
                    "标签3"
                ]
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_service.com/radios/1?expand=content%2Clabel_id_list&page=1"
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



### 电台新增
- 请求方式: `post`
- 请求地址: {host}`radios/1?expand=content,label_id_list`
- 请求参数: 
```json
{
	"content":"测试1",
	"title":"标题1",
	"radio_url":"https://www.baidu.com",
	"origin":"来源1",
	"desc": "描述1",
	"preview_image":"https://www.baidu.com",
	"status": 1,
	"participants": [1,2,3]
}
participants 是参与者的id，也就是用户的id，有多个
```
- 响应内容:  

```json

```

### 电台更新
- 请求方式: `put`
- 请求地址: {host}`radios/25`
- 请求参数: 
```json
{
	"content":"测试1",
	"title":"标题1",
	"radio_url":"https://www.baidu.com",
	"origin":"来源1",
	"desc": "描述1",
	"preview_image":"https://www.baidu.com",
	"participants": [1,2,3]
}
与文章类似
```
- 响应内容:  

```json

```


### 时间轴列表
- 请求方式: `get`
- 请求地址: {host}`radio-shafts?radio_id=1`
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
                "radio_id": 1,
                "at": 0,
                "title": "开场白",
                "content": "我是开车白",
                "quote_href": "https://www.baidu.com"
            },
            {
                "id": 2,
                "radio_id": 1,
                "at": 10,
                "title": "标题",
                "content": "内容",
                "quote_href": ""
            }
        ],
        "_links": {
            "self": {
                "href": "http://my_xijin_service.com/radio-shafts?radio_id=1&page=1"
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


### 时间轴新增
- 请求方式: `post`
- 请求地址: {host}`radio-shafts?radio_id=1`
- 请求参数: 

```json
{
	"radio_id":"2",
	"at": 0,
	"title": "开场白",
	"content": "开场",
	"quote_href":"https://www.baidu.com"
}
```
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "radio_id": "2",
        "at": 11,
        "title": "开场白1",
        "content": "开场1",
        "quote_href": "https://www.baidu.com",
        "id": 4
    }
}
```



### 时间轴更新
- 请求方式: `put`
- 请求地址: {host}`radio-shafts/3`
- 请求参数:  /3是时间轴的id

```json
{
	"radio_id":"2",
	"at": 0,
	"title": "开场白",
	"content": "开场",
	"quote_href":"https://www.baidu.com"
}
```
- 响应内容:  

```json
{
    "code": 1,
    "message": "success",
    "info": {
        "radio_id": "2",
        "at": 11,
        "title": "开场白1",
        "content": "开场1",
        "quote_href": "https://www.baidu.com",
        "id": 4
    }
}
```



### 时间轴删除
- 请求方式: `delete`
- 请求地址: {host}`radio-shafts/3`
- 请求参数:  /3是时间轴的id

```json

```
- 响应内容:  
```json
{
    "code": 1,
    "message": "删除成功",
    "info": ""
}
```
