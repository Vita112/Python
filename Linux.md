## 远程管理命令
+ 需要知道网卡和IP地址
+ ifconfig：查看本机网卡信息
+ ping：接对方IP地址，远程连接；接本机环回地址，检测网卡是否正常工作
+ SSH（secue　shell）：
> SHH服务器和SHH客户端，在linux和mac系统下默认安装；SHH客户端是一个使用SHH协议连接到远程计算机的软件程序，对所有传输文件进行加密；并且可以压缩.

`域名：IP地址的别名；IP地址：代表网络上的计算机；端口号：找到计算机上运行的应用程序（SSH服务器的端口号默认为22`


##### 常见端口号列表
|服务|端口号|
|-|-|
|SHH服务|22|
|web服务|80|
|https|445|
|ftp服务器|21|

+ SHH客户端简单使用<br>
>mac系统下登录ubuntu：`ssh [-p port] user@remote`<br>
windows系统下`putty`：安装后输入ubuntu系统的ip地址即可；`xshell`：会话窗口中点击新建，在弹出窗口中输入需要连接的主机地址，点击连接后，输入用户名。

+ scp，mac系统下远程copylinux系统下的文件&目录的命令，地址格式与ssh基本相同<br>
        拷贝文件：`scp -P port 本地文件 user@remote：远程目录`
        拷贝目录：`scp -r 当前目录 user@remote:远程目录`
  






