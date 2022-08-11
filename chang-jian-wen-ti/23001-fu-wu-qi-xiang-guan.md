## google认证如何使用？

A：参见堡垒机使用手册。

## 堡垒机中Linux系统如何上传文件？

A：在要运维的终端电脑上安装xftp软件，在堡垒机运维列表中，在该服务器操作列中选择ftp，首次提交，会弹出选择本地xftp软件路径。输入用户名密码后，浏览器调起xftp即可上传文件。

## 服务器登录不了？

A：需要联系管理员。正文包含事由、公司名称、办理内容，发送邮箱**cloudservice@avic.com**

## 密码问题等？

A：密码需妥善保存，若处理不了。发送邮箱**cloudservice@avic.com，**正文包含事由、公司名称、办理内容。

## ~~Centos操作系统，需要安装图形化桌面？~~

~~A：应用运维人员，按照网上教程安装图形化桌面即可，图形化桌面常见有GNOME等 ，还需要安装 xrdp和VNC服务。~~

## Centos服务器挂载数据盘？

1、查看当前系统磁盘挂载情况

df -h

![](/assets/d1.png)

2、 查找数据盘

fdisk -l

![](/assets/d2.png)

发现 磁盘 /dev/xvde是新增的数据盘

3、分区

fdisk /dev/xvde

输入n后回车，接下来的操作全部回车默认即可

完成后输入p，回车，查看新建分区的详细信息

接着再输入w保存，将分区结果写入分区表中

执行命令partprobe，将新的分区表变更同步至操作系统。

4、格式化

mkfs -t ext4 /dev/xvde1

5、挂载到指定目录

mount /dev/xvde1 /data

7、开机自动挂载

blkid /dev/xvde1 查看磁盘的UUID

![](/assets/d6.png)

vi /etc/fstab 编辑 /etc/fstab

![](/assets/d7.png)

保存即完成！

————————————————

## 云内yum源？

基于安全方面考虑默认情况云主机无主动访问互联网权限。云平台有针对centos7的内网yum仓库，此仓库定期同步阿里互联网yum仓库。可通过命令

```
wget http://oss-cn-beijing-zhjw-d01-a.ops.console.avic-internal.com/sw-yum/centos/centos.repo -O    /etc/yum.repos.d/centos.repo
```

下载内网yum配置文件到云主机，并删除/etc/yum.repos.d下其它.repo文件，即可访问内网yum仓库。  
如内网仓库无法满足使用，可提交访问清单按需要开通互联网访问权限。联系管理员。正文包含事由、公司名称、办理内容，发送邮箱**cloudservice@avic.com**

