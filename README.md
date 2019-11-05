# v2sub

Go 编写的用于 linux 下订阅并简单配置 [v2ray](https://github.com/v2ray/v2ray-core) 的命令行工具。

程序会创建 `/etc/v2sub.json` 文件用于存储订阅信息。

使用前需确保 v2ray.service 服务已注册且默认 v2ray 配置文件路径为 `/etc/v2ray.json`。

deepin linux 测试可用，其他系统未知。

## Features

+ 内置直接可用的配置文件和代理规则， 监听本地 socks \[1081\] 和 http \[1082\]
+ 并发测试所有节点延迟 (ping)
+ 表格形式打印所有节点

## Usage

因 ping 与 服务重启 权限需要，以root 权限运行:

```shell script
sudo ./v2sub
```

快速切换节点：

```shell script
sudo ./v2sub -ping=false -rule=false
```

更多帮助：

```shell script
./v2sub -help
```

## Warning

程序会覆盖 v2ray 配置文件。

This tool will truncate your v2ray config.