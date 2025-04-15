# ColoCrossing 独立服务器 IPMI 连接与系统安装完整指南

## 前言

本文最后更新于 2023-12-02，内容基于 ColoCrossing 99美元/年独立服务器方案撰写。

在黑色星期五促销期间，ColoCrossing 的这款高性价比独立服务器受到广泛关注。本文将详细介绍如何通过 IPMI 远程管理并安装操作系统。

## 准备工作

### 获取 IPMI 信息
1. 登录 ColoCrossing 客户面板
2. 查找 IPMI 访问信息（也可在注册邮箱中查找）
3. 检查 IPMI IP 是否与服务器网段冲突

👉 [【点击查看】2025年最新 ColoCrossing 优惠码及特价云服务器方案汇总](https://bit.ly/ColoCrossing)

## IPMI 连接步骤

### 登录 IPMI 控制台
1. 在浏览器输入 IPMI 地址
2. 下载 IPMI 连接文件备用

### Java 环境配置
- 推荐使用 Java 8U333 版本（兼容性最佳）
- 配置步骤：
  1. 安装 Java 环境
  2. 在 Java 控制面板中添加 IPMI 地址到安全例外列表
  3. 使用下载的配置文件获取完整 IPMI 地址

## 系统安装指南

### 镜像挂载方法
1. 通过 IPMI 控制台挂载 ISO 镜像
2. 重启服务器并选择从 CDROM 启动
   - 如未自动启动，需按 F11 进入引导菜单

### 使用 netboot.xyz 网络安装
- 优势：避免大文件传输，适合海外服务器
- 注意事项：
  - ColoCrossing 服务器无 IPv6 支持
  - 需手动输入 IP 信息

### Debian 系统安装示例
1. 选择网络安装选项
2. 选择 Debian 系统版本
3. 按提示完成安装流程

## 系统优化建议

### 初始登录
- 默认用户名：xidcn
- 使用 `su` 命令切换 root 账户

### 系统重装（DD）
推荐使用开源脚本进行系统重装：
bash
bash InstallNET.sh -debian 11

- 默认 root 密码：LeitboGi0ro
- 优势：去除原版系统不必要的限制

## 注意事项

1. 确保 Java 版本兼容性
2. 网络安装时需正确配置 IP 信息
3. 建议使用 SSH 密钥认证提高安全性

如需了解更多 ColoCrossing 服务器方案，可参考官方最新优惠信息。