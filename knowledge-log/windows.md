ntsd -c q -p pid### windows xp知识###

Q1: Windows XP如何查询进程的路径信息?

windows XP 系统的任务管理器无**映像路径名称**选项,无法通过任务管理器查询路径信息。我们可以通过wmic

```
#运行 cmd.exe
-------------------------
C:\Users\jack>wmic                      #运行wmic
wmic:root\cli>process                   #运行process,查看进程信息 CommandLine或者ExecutablePath


```
Q2: tasklist   taskkill  ntsd 命令如何管理进程?

1. tasklist 显示进程信息

```
Tasklist [/S system [/U username [/P [password]]]] [/M [module] | /SVC | /V] [/FI filter] [/FO format] [/NH]

//查看远程系统的进程
#tasklist /s 218.22.123.26 /u jtdd /p 12345678

//查看系统进程提供的服务
#tasklist /svc

//查看调用DLL模块文件的进程列表
#tasklist /m shell32.dll

//使用筛选器查找指定的进程
#tasklist /FI "USERNAME ne NT AUTHORITY\SYSTEM" /FI "STATUS eq running"

```
2. taskkill 关闭进程

```
TASKKILL [/S system [/U username [/P [password]]]]
         { [/FI filter] [/PID processid | /IM imagename] } [/F] [/T]

         描述:
             这个命令行工具可用来结束至少一个进程。
             可以根据进程 id 或图像名来结束进程。


#TASKKILL  /pid 1132
#TASKKILL /PID 1230 /PID 1241 /PID 1253 /T
#TASKKILL /F /IM notepad.exe /IM mspaint.exe

```

3. ntsd(nt system debugger) 关闭进程

```
//根据PID关闭进程
#ntsd -c q -p pid   

//根据"进程名"关闭进程    
#ntsd -c q -pn  ***.exe       

```
