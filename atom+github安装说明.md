#### 1.安装文件准备####

操作系统: Windows Win10  64位

|位置|下载路径|文件列表
|:------|:------|:------|
|百度云盘(Username: njjack1987) |我的云盘/软件开发/web前端html+js/开发环境/win10|AtomSetup.exe、atom-packages.rar、Git-2.11.0-32-bit.exe|

#### 2.安装说明####

>1. 下载AtomSetup.exe、atom-packages.rar、Git-2.11.0-32-bit.exe
>2. 运行AtomSetup.exe，安装Atom环境
>3. 解压缩atom-packages.rar到** C:\\Users\\[用户名]\\.atom\\packages **
>4. 运行Git-2.11.0-32-bit.exe，安装Git环境


#### git使用

```
$git   init            //初始化
$ git commit -m 'add'               //添加
[master ea4cbaa] add
 7 files changed, 142 insertions(+), 5 deletions(-)
 create mode 100644 "atom+github\345\256\211\350\243\205\350\257\264\346\230\216.md"
 create mode 100644 job-log/20161205.md
 create mode 100644 job-log/20161206.md
 create mode 100644 job-log/rp-config.md
 create mode 100644 job-log/todo-list.md
 create mode 100644 knowledge-log/windows.md

 $ git push origin master                 //提交到远程
 Enter passphrase for key '/c/Users/jack/.ssh/id_rsa':
 Counting objects: 11, done.
 Delta compression using up to 4 threads.
 Compressing objects: 100% (9/9), done.
 Writing objects: 100% (11/11), 2.95 KiB | 0 bytes/s, done.
 Total 11 (delta 1), reused 0 (delta 0)
 remote: Resolving deltas: 100% (1/1), completed with 1 local objects.
 To github.com:njjackzhong/notebook.git
    7fb72d6..ea4cbaa  master -> master


```

_________

Q1:  如果提示

>$ git commit  

>  Please tell me who you are.  

>Run

>  git config --global user.email "you@example.com"

>  git config --global user.name "Your Name"

表示没有用户或者邮件信息，请按照提示配置user.name和user.email即可，完成后效果如下

```
$ git config --list --global | grep user
user.email=njjackzhong@126.com
user.name=njjackzhong

$ git config --list --local | grep user
$



```
