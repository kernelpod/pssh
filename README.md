# Parallel SSH (PSSH)

PSSH (Parallel SSH) 是一个用于在多个远程主机上并行执行命令的工具集。它提供了OpenSSH和相关工具的并行版本，包括pssh、pscp、prsync、pnuke和pslurp。

## 功能特点

- 并行执行SSH命令
- 并行文件传输
- 支持密码认证和密钥认证
- 支持自定义超时和并行度
- 支持输出重定向
- 支持彩色输出

## 系统要求

- Python 3.6 或更高版本
- OpenSSH 客户端

## 安装

```bash
# 从源码安装
python3 setup.py install
```

## 使用方法

### 1.常用选项

- `-h, --hosts`: 指定主机列表文件
- `-H, --host`: 指定单个主机
- `-l, --user`: 指定用户名
- `-p, --par`: 设置并行度
- `-t, --timeout`: 设置超时时间（秒）
- `-o, --outdir`: 指定标准输出目录
- `-e, --errdir`: 指定标准错误输出目录
- `-A, --askpass`: 启用密码认证
- `-i, --inline`: 内联显示每个服务器的输出
- `-P, --print`: 实时打印输出

### 2. 环境变量

- `PSSH_USER`: 默认用户名
- `PSSH_PAR`: 默认并行度
- `PSSH_OUTDIR`: 默认输出目录
- `PSSH_ERRDIR`: 默认错误输出目录
- `PSSH_TIMEOUT`: 默认超时时间
- `PSSH_VERBOSE`: 启用详细输出
- `PSSH_ASKPASS`: 启用密码认证

## 注意事项

1. 确保目标主机可以通过SSH访问
2. 建议使用SSH密钥认证以提高安全性
3. 合理设置并行度，避免对目标主机造成过大负载
4. 使用超时选项避免命令长时间挂起

## 许可证

BSD License 