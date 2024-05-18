# 模型

### User 用户

| 字段名/继承               | 类型                 | 含义         |
| -------------------- | ------------------ | ---------- |
| ResourceWithState    | -                  |            |
| ResourceWithDescribe | -                  |            |
| planet\_code         | int                | 神厨星球代码     |
| kof\_id              | string             | 朋厨 ID      |
| password             | string             | 加密保存的密码    |
| tel                  | string             | 电话号码       |
| tel\_validated       | bool               | 电话号码是否已经验证 |
| tel\_valid\_method   | string             | 电话号码验证方法   |
| wx\_open\_id         | string             | 微信开放 ID    |
| wx\_session\_key     | string             | 微信会话密钥     |
| inner\_id            | primitive.ObjectID | 朋厨主星球 ID   |
| out\_sync\_to\_inner | bool               | 是否向本星同步    |
| inner\_sync\_to\_out | bool               | 是否向外星同步    |



