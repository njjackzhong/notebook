____________

本文主要是记录Intellij IDEA 14.1.4 使用过程中遇到的各种问题。

Q1: Intellij IDEA 14.1.4   启动报错:
>Error  8 artifacts cannot be.You can remove them from the project(no files will be deleted).

>module 1: Unkown artifact type: exploded-war

>module 2: Unkown artifact type: war

>module 3: Unkown artifact type: exploded-war

或者 Project Structure(Ctrl+Alt+Shift+S)--->Artifacts--->Cannot load artifact. Unkown artifact type: exploded-war.

解决问题：
> Ctrl+Alt+S  打开Settings窗口

> 打开Pluggings选项卡，搜索关键字** Java EE**

> 启用** Java EE EJB,JPA,Servlets ** 插件
