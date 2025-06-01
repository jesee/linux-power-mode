## 使用说明

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

## 命令行使用
- 通过终端直接运行：
  ```bash
  power-mode-set
  ```
- 或通过创建的菜单项图形化操作
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
