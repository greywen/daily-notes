## ubuntu安装docker compose
1. 下载安装文件
```bash
curl -L "https://github.com/docker/compose/releases/download/v2.29.7/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
2. 设置文件夹权限
```bash
chmod +x /usr/local/bin/docker-compose
```

3. 验证
```bash
docker compose version
```

## 常用命令
- 更新docker-compose.yml文件重启
```bash
docker-compose up --force-recreate -d
```