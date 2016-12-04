# DataPlatform 常识

---

#### Q1: ActionPlatformClient.exe文件管理无法导出fastdfs文件，提示“导出文件失败！”或者导出文件的大小是0字节？

方法1：查看日志
> 1. 查看 **ActionPlatformClient** Logs/log.txt 日志文件，初步定位问题
> 2. 查看**DataPlatformDALHessian**日志文件，确认是否已经正确返回**fileUrl**给ActionPlatformClient客户端
> 3. 查看**DataPlatformDriveService**日志文件，确认是否上传文件至fastdfs( **注意** fastdfs config文件位置: classes/fdfs_conf)

方法二：浏览器测试

> 1. 查看**mysql存储服务**的dataplatform.file表数据，查询文件存储在fastdfs的索引Id，即**fileurl**,类似group001/M00/001/001/HXJAKSJKAHSKAHSUIAU.jpg
> 2. 打开浏览器，地址栏输入http://192.201.201.206/fileUrl/ 如果可以下载并预览文件，则文件已经upload至fastdfs，同时fastdfs正确提供了web访问服务


#### Q2: appache tomcate 管理

##### (1)如何使用命令行关闭tomcat7服务?

```
 ** 1.windows环境 **

#tasklist  | findstr tomcat        '查询tomcat7服务'

映像名称                      PID 会话名              会话#      内存使用

=========================================================================

 tomcat7.exe                   8720                Services       10020KB   

#taskill  89720  or net stop Tomcat7       '关闭tomcat7服务'


#net start Tomcat7     '启动tomcat7服务'

 ** 2.linux环境 **

```

##### (2)如何启用tomcat7-web管理功能?




#### Q3: fastdfs如何命令行管理？如何查询当前文件数目与存储文件等信息?



----
## 计划

> 任务一   2016-12-3 厦门   DataPlatformDriveService 备份至本地，同时上传svn




# 附录
| 角色名称  | IP地址  | 部署模块  |日志文件配置|
|:----------|:-------|:---------|:----------|
|文件存储服务|192.201.201.206|fastdfs  + nginx webserver|2|
|webservice服务|192.201.201.203|DataPlatformDALHessian  + DataPlatformWebService|1|
|mysql存储服务|192.201.201.207|mysql db server|3|
|数据驱动服务|192.201.201.210|DataPlatformDriveService|4|
