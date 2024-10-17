## Windows 优先使用IPv4而非IPv6
为什么需要优先使用IPv4？因为翻墙不支持IPv6，但电脑会优先使用IPv6，不让电脑优先使用IPv4会导致偶尔翻墙失败或者翻墙速度非常慢。

- 使用管理员权限打开cmd
```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip6\Parameters" /v DisabledComponents /t REG_DWORD /d 0x20 /f
```
- 重启电脑

#### 恢复原状
```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip6\Parameters" /v DisabledComponents /t REG_DWORD /d 0x0 /f
```

#### 禁用临时IPv6地址

```powershell
netsh interface ipv6 set global randomizeidentifiers=disabled
```

```powershell
netsh interface ipv6 set privacy state=disabled
```
