
#### RP服务管理模块



|角色|访问地址|Web用户信息|系统用户信息|
|:----|:-----|:----|:----|
|Cloulera Web Manager|http://192.201.203.12:7180/|admin admin|root  841_sjzc|
|Impala SQL Web Page |http://192.201.203.12:8888/|admin admin|root  841_sjzc|
|nodejs  web server  |http://192.201.203.21:3000/|test 123456|root 841_sjzc|

### Nodejs

Q1: ** nodejs **  web  server |IP等于192.201.203.21 |  服务方式运行

```
//mobaXterm or ssh 连接 192.201.203.21

//切换到nodejs部署目录
#cd /opt/publish/nj_nova_1/devtools

//运行pm2的脚本
#sh hook_publish.sh       
```

K2: ** 823admin.tbl_system_config ** 配置信息存储

包括HDFS 结构化、非结构化文件路径  GIS地图服务器地址、综合应用服务器地址、消息转发等;
其他模块，例如CloudPersonCore人立方等

### Cloulera  CDH

Q1: ** impala ** SQL 语句
