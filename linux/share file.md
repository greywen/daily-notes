## 共享文件
1. 安装 samba
```bash
sudo apt install samba
```
2. 设置共享目录
```bash
sudo vim /etc/samba/smb.conf
```

3. 修改配置
```txt
[share]
path = /app/xx  目录
browsable = yes 是否可以浏览
guest ok = yes  允许匿名访问
read only = no  只读
writable = yes  可写
valid user = username 设置访问用户名
```

4. 设置访问用户密码
```bash
sudo smbppasswd -a username
```

5. 重启服务
```bash
sudo systemctl restart smbd
```

6. 访问
Windows 访问 \\192.168.1.x\share 输入账号密码


## 错误处理
1. Windows 不能访问此共享文件夹，因为你组织的安全策略阻止....

本地安全策略->管理模板->网络->Lanman 工作站->启用不安全的来宾登录