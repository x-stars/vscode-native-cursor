# Visual Studio Code 原生样式指针

本项目旨在将 [Visual Studio Code](https://code.visualstudio.com/) 的鼠标指针修改为符合原生应用的样式。

## 项目缘起

Visual Studio Code 的界面采用 [Electron](https://www.electronjs.org/) 技术构建，符合网页元素的逻辑，几乎所有可点击控件的指针样式均为手型指针 `cursor: pointer`；而原生应用对于链接以外的控件均使用普通指针 `cursor: default`，这使得 Visual Studio Code 作为桌面应用，其指针样式却显得格格不入。

关于 Visual Studio Code 鼠标指针样式问题的详情，请参考此文章（同时也是本项目的灵感来源）：[WebApp for Desktop: 请不要滥用手型指针](https://zhuanlan.zhihu.com/p/40831426)

## 使用方法

本项目仅包含两个 PowerShell 脚本文件，分别用于指针样式的修改和还原：

* [`Set-VSCodeNativeCursor.ps1`](scripts/Set-VSCodeNativeCursor.ps1) 设置原生指针样式
* [`Reset-VSCodeCursor.ps1`](scripts/Reset-VSCodeCursor.ps1) 还原原始指针样式

**注意**：如果 Visual Studio Code 安装在系统目录下（如 Windows 的 `Program Files` 目录等），则需要管理员权限运行。

## 已知问题

由于此脚本修改了 Visual Studio Code 的核心资源文件，因此使用后会导致出现安装损坏警告，标题也会出现不受支持的提示；此警告将在使用还原脚本还原设置后消除。

## 平台兼容性

目前此项目仅对 Windows 平台的 1.56 版本进行过测试。

PowerShell 脚本也能用于 macOS 和 Linux 平台（需要另行[安装 PowerShell](https://github.com/PowerShell/PowerShell/releases)），但脚本效果目前并未测试确认。
