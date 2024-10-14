## chown (change owner) 更改文件或目录的所有者或所属组

- 基本格式
```bash
chown [新所有者]:[新组] [文件/目录]
```

- 更改文件所有者
```bash
chown target_user filename
```

- 更改目录及其内容的所有者
```bash
chown -R target_user directory
```

## chmod (change mode) 更改文件或目录的权限

#### 权限类型数字表示
- 读 (r)：4
- 写 (w)：2
- 执行 (x)：1
#### 权限数组表示
- 第一组（所有者，u）
- 第二组（组用户，g）
- 第三组（其他用户，o）

- 基本格式
```bash
chmod [权限字符串] [文件/目录]
```

- 更改目录及其内容的权限
```bash
chmod -R 755 directory
```
- 第一位 7（4+2+1，所有者拥有读、写、执行权限）
- 第二位 5（4+0+1，组用户拥有读和执行权限）
- 第三位 5（4+0+1，其他用户拥有读和执行权限）
