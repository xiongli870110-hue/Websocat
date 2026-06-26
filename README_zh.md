# Websocat

Websocat 是一个命令行 WebSocket 客户端和服务器。本仓库包含为 Linux 环境编译的 websocat 预构建版本。

## 功能特性

✅ 在 Ubuntu 22.04 运行器内构建  
✅ 包含 WebSocket 客户端/服务器功能  
✅ 兼容大多数现代 Linux 发行版  
✅ 易于安装的二进制分发版本

## 安装

### 前置要求

- Linux 系统（兼容 Ubuntu 22.04 及类似发行版）
- `wget` 或 `curl` 用于下载版本
- `tar` 用于解压存档
- `sudo` 权限以安装到 `/usr/local/bin`

### 安装步骤

按照以下命令安装 websocat：

```bash
# 下载版本
wget https://github.com/xiongli870110-hue/Websocat/releases/download/websocat-1.13.0/websocat-build.tar.gz

# 解压存档
tar -xzf websocat-build.tar.gz

# 复制二进制文件到系统路径
sudo cp output/websocat /usr/local/bin/websocat

# 使二进制文件可执行
sudo chmod +x /usr/local/bin/websocat

# 验证安装
websocat --version
```

## 构建信息

### 版本信息
- **版本号**: 1.13.0
- **基础系统**: Ubuntu 22.04
- **构建日期**: 详见发行版页面

### 构建环境

构建过程包括：

1. **系统依赖**
   - `build-essential` - 基本构建工具
   - `curl` 和 `git` - 用于下载源代码和版本控制
   - `pkg-config` - 库配置工具
   - `libssl-dev` - OpenSSL 开发文件
   - `rustc` 和 `cargo` - Rust 编译器和包管理器

2. **构建流程**
   - 从 https://github.com/vi/websocat.git 克隆原始 websocat 仓库
   - 使用 `cargo build --release` 编译
   - 将二进制文件打包成可分发的 tarball

3. **输出内容**
   - 针对发行版优化的预编译二进制文件
   - 在目标系统上无需编译即可使用的可执行文件

## 使用方法

安装后，可以从任何终端使用 websocat：

```bash
# 查看版本
websocat --version

# 根据需要使用 WebSocket 客户端/服务器
websocat [OPTIONS] [ARGUMENTS]
```

## 故障排除

### 权限被拒绝错误
如果在运行 websocat 时收到"权限被拒绝"错误，请确保它拥有可执行权限：
```bash
sudo chmod +x /usr/local/bin/websocat
```

### 下载失败
如果下载失败，请验证：
- 互联网连接是否正常
- 版本是否仍存在于：https://github.com/xiongli870110-hue/Websocat/releases/download/websocat-1.13.0/websocat-build.tar.gz
- 是否有足够的磁盘空间

### 兼容性问题
如果 websocat 在您的系统上无法运行，请确保使用的是与 Ubuntu 22.04 兼容的 Linux 发行版（例如 Debian、Ubuntu 20.04+等）。

## 相关链接

- **原始项目**: https://github.com/vi/websocat
- **发行版页面**: https://github.com/xiongli870110-hue/Websocat/releases
- **构建工作流**: https://github.com/xiongli870110-hue/Websocat/actions

## 许可证

请参考原始 websocat 项目的许可证信息：https://github.com/vi/websocat

## 支持

如有关于此构建版本或安装的问题，请在本仓库中提交 Issue。  
如有关于 websocat 本身的问题，请参考原始项目：https://github.com/vi/websocat
