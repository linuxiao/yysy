# 场景模拟

公司A，部署一套前后端分离的应用，应用名称质量系统，对外以app.abc.com域名发布，在商密网上，最终用户访问到的是[https://app.abc.com。](https://app.abc.com。)

# 实施过程

## 1、申请开通服务器资源

例如：需要开通2台4核8G/100G系统/500G数据盘ECS。运维人员张三、李四。

填下[**《商网专有云-应用部署资源申请》**](/assets/xxxx系统-商网专有云-应用部署资源申请-V3.0.xlsx)发送邮箱**cloudservice@avic.com，并抄送相关商务。**![](/assets/示例2.png)运维办理后，会回复邮件。里面附带Excel，输入密码后，可以看到2台服务器的IP地址，账号密码。

商网-质量系统应用01，10.x.x.2，user/password。vpn的账号密码及登录地址。

## 2、部署应用

### 2.1，登录vpn及堡垒机。

1.下载VPN客户端[https://43.254.89.14:8443/](https://43.254.89.14:8443/)，下载完成后“**以管理员身份运行**”安装。

![](file:///C:\Users\Lenovo\AppData\Local\Temp\ksohtml4816\wps1.jpg)



2.登陆VPN，使用分配的用户名及初始密码登录，首次登录需提交终端绑定，修改个人密码。

![](file:///C:\Users\Lenovo\AppData\Local\Temp\ksohtml4816\wps2.jpg)

![](file:///C:\Users\Lenovo\AppData\Local\Temp\ksohtml4816\wps3.jpg)

![](file:///C:\Users\Lenovo\AppData\Local\Temp\ksohtml4816\wps4.jpg)

![](file:///C:\Users\Lenovo\AppData\Local\Temp\ksohtml4816\wps5.jpg)



3.点击堡垒机访问链接

![](file:///C:\Users\Lenovo\AppData\Local\Temp\ksohtml4816\wps6.jpg)

![](file:///C:\Users\Lenovo\AppData\Local\Temp\ksohtml4816\wps7.jpg)



4.堡垒机操作详见堡垒机用户手册

### 2.2，登录服务器。

### 2.3，上传安装文件。

### 2.4，安装部署软件。

### 2.5，导入数据库数据文件。

### 2.6，验证部署完成。

### 2.7，申请应用漏扫。

## 3、安全整改

3.1，修复漏扫问题。

3.2，申请复测。

## 4、解析上线

4.1，协助购买SSL证书

4.2，设置解析

