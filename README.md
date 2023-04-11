# mprpc

## 开发环境

- Linux version 3.10.0（CentOS 7.9 64位）
- gcc version 7.3.0
- cmake version 2.8.12.2
- zookeeper version 3.4.10

## 编译

```shell
# 项目编译执行即可 头文件生成至目录./lib/include，.a库文件生成至目录./lib
sudo ./autobuild.sh

# 测试用例进入bin/文件夹，provider为服务提供者，consumer为服务消费者。
cd ./bin
./provider -i test.conf
./consumer -i test.conf
```

## 项目内容

1. 使用muduo网络库作为项目的网络核心模块，提供高并发网络的I/O服务，解耦网络和业务模块
2. 使用protobuf序列化和反序列化消息作为私有通信协议
3. 使用zookeeper进行分布式应用程序协调服务，实现框架的分布式通信，提高后端服务的并发能力。

## mprpc的解析

![](./1.png)

![](C:\Users\GUANJIAA\Desktop\微信图片_20230411170933.png)

## 收获

熟悉了基于开源网络库进行框架的设计，掌握了protobuf的序列化和反序列化，zookeeper的命名服务的配置。
