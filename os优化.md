## 话题一：win10系统资源优化

---
#### Q0: how to disable startup applications?
> step1: 启动**任务管理器**

> step2: **启动** tab分页,禁用应用程序，例如迅雷、迅雷快鸟等

#### Q1: Win10 CompactTelRunner.exe，在系统开机启动占用硬盘Cycle，导致系统响应非常缓慢？

```
#net stop DiagTrack   "关闭用户体验中心服务"
```

#### Q2: Win修改cmd字体?

```
step1: 下载字体, http://files.cnblogs.com/files/kischn/Microsoft_YaHei_Mono.7z
step2: 安装字体, 解压缩 Microsoft YaHei Mono.ttf  至 C:\Windows\Fonts
step3: 修改注册表
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Console\TrueTypeFont]  "936"="*Microsoft YaHei Mono"


```

#### Q3:localservicenetworkrestricted high disk cycle on OS init?

```
#运行 services.msc   
#设置"Diagnostic Policy Service",即DPS服务,启动方式"禁用"
#重启系统
```

---
