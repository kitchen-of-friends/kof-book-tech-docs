# 模型

### ResourceWithIdAndAudit 有ID、可审计资源（基础类）

该基类让数据拥有ID，且可用记录创建人、修改人、创建时间、修改时间，所有深度社交协议资源都会继承该基类。

<table><thead><tr><th width="196">字段名</th><th>类型</th><th>含义</th></tr></thead><tbody><tr><td>name</td><td>string</td><td>名称</td></tr><tr><td>logo</td><td>string</td><td>logo 存储 url</td></tr><tr><td>content</td><td>string</td><td>内容/描述</td></tr><tr><td>img_list</td><td>[]string</td><td>图片列表</td></tr><tr><td>video_list</td><td>[]string</td><td>视频列表</td></tr></tbody></table>



### ResourceWithDescribe 可描述资源（基础类）&#x20;

该基类让资源具有名字、Logo、描述型文本、图片列表、视频列表，如活动、组织、线上内容等资源都会继承该基类。

| 字段名         | 类型        | 含义          |
| ----------- | --------- | ----------- |
| name        | string    | 名称          |
| logo        | string    | logo 存储 url |
| content     | string    | 内容/描述       |
| img\_list   | \[]string | 图片列表        |
| video\_list | \[]string | 视频列表        |



### ResourceWithLoc 有地理信息的资源（基础类）&#x20;

如一些资源需要带有地理位置信息，则需要继承该资源；该资源支持 “is\_virtual” 属性，代表那条数据无地理信息，当为 true 时，可忽略当条数据的地理请求。

| 字段名                  | 类型         | 含义                 |
| -------------------- | ---------- | ------------------ |
| is\_virtual          | bool       | 是否是线上的             |
| loc\_info.address    | string     | 地址信息               |
| loc\_info.name       | string     | 地点名称               |
| loc\_info.combine    | string     | 上述二者拼接在一起          |
| loc\_geo.type        | string     | 地理位置类型，一般都是“Point” |
| loc\_geo.coordinates | \[]float64 | 两个数值，第一个是经度，第二个是纬度 |
