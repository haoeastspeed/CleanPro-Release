<div align="center">

# 极净 CleanPro

**专业级 Windows 系统清理 · 软件卸载 · 系统修复工具**

绿色单文件 · 双击即用 · 无需安装 · 支持 Windows 10 / 11

[![下载最新版](https://img.shields.io/badge/下载-最新版本-2f9e8f?style=for-the-badge)](https://github.com/haoeastspeed/CleanPro-Release/releases/latest)
[![系统](https://img.shields.io/badge/系统-Windows%2010%20%2F%2011-0078d4?style=flat-square)](https://github.com/haoeastspeed/CleanPro-Release/releases/latest)
[![版本](https://img.shields.io/badge/版本-4.6.0-2f9e8f?style=flat-square)](https://github.com/haoeastspeed/CleanPro-Release/releases)
[![许可](https://img.shields.io/badge/许可-免费使用-lightgrey?style=flat-square)](LICENSE)

</div>

---

## 简介

**极净 CleanPro** 是一款专注于「**清理、卸载、修复**」三大核心能力的 Windows 系统管理工具。
无需安装、不捆绑、不弹广告、不收集任何个人数据，一个单文件即可完成专业清理软件的绝大多数工作，让电脑保持干净、流畅。

> 软件成品（可执行文件）在此公开发布；源代码不公开。所有发布的可执行文件均经过 **SHA256 校验**与**数字签名**，可放心使用。

## 核心功能

### 一、深度清理

- **系统垃圾**：系统 / 用户临时文件、Windows 更新缓存、错误报告、日志、内存转储、缩略图与字体缓存、`.chk` 磁盘扫描遗留等
- **安全机制**：默认**不清空回收站、不清理预读取（Prefetch）**；休眠文件、页面文件、系统组件（WinSxS）等关键项绝不手动删除
- **常用软件缓存**：覆盖数十款常用软件的可再生缓存
- **浏览器专清**：Chrome、Edge、Firefox 及国产双核浏览器的缓存；Cookie 支持白名单保护登录态
- **聊天软件专清**：微信、QQ、钉钉、企业微信、飞书的缓存（**聊天记录、接收文件、登录数据绝不清理**）
- **隐私痕迹**：跳转列表、最近文档、运行记录、地址栏历史、通知图标历史等（可选）
- **空间分析**：磁盘占用可视化、大文件、重复文件、空文件夹扫描，一键定位空间占用

### 二、智能卸载

- 调用软件**官方卸载程序**完成常规卸载，干净可靠
- **强制卸载**：针对损坏、无法正常卸载或恶意软件，清除其安装目录、缓存与注册表项
- **残留一键清理**：卸载后自动扫描并清理遗留文件、文件夹与注册表信息
- 卸载信息只读展示，系统关键组件受保护、不可误删

### 三、修复与优化

- **注册表清理与修复**：无效键值、已卸载软件残留、失效文件关联、无效卸载信息、失效快捷方式等；**清理前自动整键备份，可一键还原**
- **系统修复向导**：汇集 Windows 常见问题的一键修复，系统文件校验（SFC / DISM）入口
- **启动项管理**：开机启动项、服务、计划任务的检测、禁用与删除，附启动影响评级
- **右键菜单管理**：可查看 / 禁用多余右键菜单项，操作可逆
- **系统还原**：还原点创建、查询与安全保护设置
- **文件占用解锁**：基于 Windows Restart Manager，安全解除被占用的文件 / 文件夹

## 安全设计

| 原则 | 说明 |
| --- | --- |
| 只清可再生内容 | 仅清理缓存、临时文件等可由系统 / 软件重新生成的数据 |
| 关键数据受保护 | 聊天记录、接收文件、书签、密码、登录态、网盘同步文件等绝不作为垃圾 |
| 删除前可备份 | 注册表等操作删除前自动备份，支持一键回滚 |
| 权限最小化 | 不注册为防病毒、不获取 SYSTEM 内核权限、不关闭安全软件 |
| 不收集数据 | 不联网上传任何个人信息；仅在「检查更新」时访问本发布仓库 |
| 签名与校验 | 发布文件经数字签名；自动更新须通过 SHA256 + 签名证书双重校验 |

## 系统要求

- **操作系统**：Windows 10、Windows 11（64 位；同时兼容 32 位）
- **权限**：部分清理 / 卸载操作需**管理员权限**（右键“以管理员身份运行”）
- **运行库**：内置 Windows 自带的 .NET Framework 4.8（绝大多数系统已预装）
- 无需安装、不写常驻进程、不占用后台资源

## 下载与使用

1. 前往 **[Releases 发布页](https://github.com/haoeastspeed/CleanPro-Release/releases/latest)**
2. 下载 `极净 CleanPro.exe`（单文件）
3. 右键“**以管理员身份运行**”，按界面提示扫描、勾选并清理
4. 建议首次使用先查看软件内「**使用帮助**」

### 校验文件完整性（可选）

发布页同时提供 `.sha256` 校验文件。PowerShell 中执行：

```powershell
Get-FileHash ".\极净 CleanPro.exe" -Algorithm SHA256
```

将结果与 `.sha256` 文件中的值比对，一致即未被篡改。

## 自动更新

软件支持自动检查更新（可在设置中关闭）：

- 默认仅在发现新版本时**轻提示**，**不会自动下载安装**
- 用户确认后才下载，并在 **SHA256 与数字签名双重校验通过**后自动替换、重启
- 更新不会删除您的设置、备份与白名单

## 版本历史

详见 **[Releases](https://github.com/haoeastspeed/CleanPro-Release/releases)**。

## 免责声明

本软件免费提供，按“现状”分发。清理与修复操作虽经过严格安全设计，仍建议在执行重要操作前备份重要数据、创建系统还原点。因使用本软件造成的任何直接或间接损失，作者不承担责任。

---

<div align="center">

**极净 CleanPro** · 让 Windows 保持干净流畅

[产品主页](https://haoeastspeed.github.io/CleanPro-Release/) · [下载最新版](https://github.com/haoeastspeed/CleanPro-Release/releases/latest)

</div>
