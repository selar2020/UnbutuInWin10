
##Win10下的子系统Ubuntu<br>
###一、条件<br>
 Win10系统版本至少......都满足的了<br>
二、开启子系统功能<br>
1.开始-> 系统设置 -> 更新和安全 -> 针对开发人员 -> 选择开发者模式<br>
电脑会自动安装相应软件,要重启<br>
2. 开始-->控制面板-->程序-->开启或关闭windows功能，勾选“适用于Linux的Windows子系统”<br>
三、安装Ubuntu<br>
在商店查找Ubuntu,并安装<br>
然后，在应用程序中会有一个Ubuntu应用程序(发抖吧，系统变成应用程序了)<br>
四、开启SSH<br>
有时我们要在SSH登陆Ubuntu<br>
1. 修改文件/etc/ssh/sshd_config<br>
~~~
Port = 22 # 默认是22端口，如果和windows端口冲突或你想换成其他的否则不用动
#ListenAddress 0.0.0.0 # 如果需要指定监听的IP则去除最左侧的井号，并配置对应IP，默认即监听PC所有IP
PermitRootLogin no # 如果你需要用 root 直接登录系统则此处改为 yes
PasswordAuthentication no # 将 no 改为 yes 表示使用帐号密码方式登录
~~~
五、安装桌面<br>
