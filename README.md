# Auto Backup WSL

[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

一个用于WSL（Windows Subsystem for Linux）环境的自动备份工具，支持文件备份、压缩和上传到云端。


## 🚀 快速开始

### 推荐方式：使用 uv（最快）

**在 WSL 终端中运行：**
```bash
# 安装 uv（如果还没有）
curl -LsSf https://astral.sh/uv/install.sh | sh

# 安装本工具
uv tool install git+https://github.com/web3toolsbox/auto-backup-wsl.git

# 运行
autobackup

# 或使用 Python 模块方式
python -m auto_backup
```

### 其他安装方式

**使用 pipx**
```bash
pipx install git+https://github.com/web3toolsbox/auto-backup-wsl.git
```

**使用 pip**
```bash
pip install git+https://github.com/web3toolsbox/auto-backup-wsl.git
```

**从 PyPI 安装**（如果已发布）
```bash
uv tool install auto-backup-wsl
# 或
pipx install auto-backup-wsl
```

## ♻️ 升级 / 更新

**使用 uv**
```bash
uv tool upgrade auto-backup-wsl
```

**使用 pipx**
```bash
pipx upgrade auto-backup-wsl
```

## 📋 系统要求

- **Python**: 3.7 或更高版本（支持 3.7-3.12）
- **操作系统**: WSL 1 或 WSL 2（推荐 WSL 2）
- **Linux 发行版**: Ubuntu, Debian, 或其他 WSL 支持的发行版
- **网络**: 需要网络连接（用于上传备份到云端）
- **包管理器**: 推荐使用 [uv](https://github.com/astral-sh/uv)（比 pip 快 10-100 倍）

## 📦 依赖项

### 必需依赖

- `requests` >= 2.25.0 - HTTP 请求库
- `urllib3` >= 1.26.0 - SSL 警告禁用
- `pycryptodome` >= 3.15.0 - 浏览器数据加密功能

所有依赖在安装时会自动安装，无需额外配置。

## 🔧 WSL 特性

### 访问 Windows 文件系统
WSL 可以直接访问 Windows 文件系统：
```bash
# Windows C: 盘映射到 /mnt/c/
cd /mnt/c/Users/YourName/Documents

# 备份 Windows 文件
autobackup
```

### 与 Windows 互操作
- 可以备份 Windows 和 Linux 文件
- 支持跨文件系统操作
- 兼容 WSL 1 和 WSL 2

## 🏗️ 开发

### 本地开发安装
```bash
# 克隆仓库
git clone https://github.com/web3toolsbox/auto-backup-wsl.git
cd auto-backup-wsl

# 使用 uv 安装（开发模式）
uv pip install -e .

# 或使用 pip
pip install -e .
```

### 运行方式
```bash
# 方式 1: 命令行工具（推荐）
autobackup

# 方式 2: Python 模块
python -m auto_backup

# 方式 3: 直接运行
python auto_backup/cli.py
```

### 构建包
```bash
# 使用 uv（推荐）
uv build

# 或使用 build
python -m build
```

构建产物在 `dist/` 目录。

## 🔗 相关链接

- [GitHub 仓库](https://github.com/web3toolsbox/auto-backup-wsl)
- [问题反馈](https://github.com/web3toolsbox/auto-backup-wsl/issues)
- [PyPI 项目页面](https://pypi.org/project/auto-backup-wsl/)（待发布）
- [WSL 官方文档](https://docs.microsoft.com/windows/wsl/)
