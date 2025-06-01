以下是对您提供的Markdown文档的优化版本，使用了标准的Markdown语法和清晰的格式分层：

```markdown
# 电源模式切换工具使用指南

## 适用系统
- Debian
- Ubuntu
- Linux Mint

## 安装步骤

1. 将 `power-mode-set` 文件复制到 `/usr/local/bin` 目录：
   ```bash
   sudo cp power-mode-set /usr/local/bin/
   ```

2. 赋予可执行权限：
   ```bash
   sudo chmod +x /usr/local/bin/power-mode-set
   ```

## 添加菜单项（适用于Linux Mint XFCE）

1. 创建桌面入口文件：
   ```bash
   vim ~/.local/share/applications/power-mode.desktop
   ```

2. 添加以下内容：
   ```ini
   [Desktop Entry]
   Name=电源模式
   Comment=切换电源性能模式
   Exec=xfce4-terminal --title="电源模式切换" --hold -e "/usr/local/bin/power-mode-set"
   Icon=preferences-system-power
   Terminal=false
   Type=Application
   Categories=System;
   ```

3. 完成后即可在系统菜单中找到"电源模式"选项。

## 使用说明
- 通过终端直接运行：
  ```bash
  /usr/local/bin/power-mode-set
  ```
- 或通过创建的菜单项图形化操作
```

优化说明：
1. 增加了文档标题和清晰的章节划分
2. 使用代码块包裹命令和配置文件内容，提高可读性
3. 统一了代码块的语法标记（```）
4. 将步骤分解得更清晰，增加编号
5. 添加了使用说明部分
6. 保持了原有的所有技术信息
7. 使用标准的Markdown列表和代码块格式

这样的格式更容易阅读和理解，同时也保持了技术文档的准确性。
