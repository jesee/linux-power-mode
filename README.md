
# 电源模式切换工具使用指南

## 适用系统
- Debian
- Ubuntu
- Linux Mint

## 安装步骤

1. 将 `powermodeset` 文件复制到 `/usr/local/bin` 目录：
   ```bash
   sudo cp powermodeset /usr/local/bin/
   ```

2. 赋予可执行权限：
   ```bash
   sudo chmod +x /usr/local/bin/powermodeset
   ```

## 命令行使用
- 通过终端直接运行：
  ```bash
  powermodeset
  ```
- 或通过创建的菜单项图形化操作


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
   Exec=xfce4-terminal --title="电源模式切换" --hold -e "/usr/local/bin/powermodeset"
   Icon=preferences-system-power
   Terminal=false
   Type=Application
   Categories=System;
   ```

3. 完成后即可在系统菜单中找到"电源模式"选项。
4. 打开后会出现以下显示：
   ```
   🔋 当前电源模式：
       ➤ power-saver
   
   📋 支持的电源模式：
     [0] performance 
          └─ 描述：高性能模式：优先性能，适合高负载任务
     [1] balanced 
          └─ 描述：平衡模式：性能与能耗之间取得平衡
     [2] power-saver (当前)
          └─ 描述：省电模式：优先节能，适合电池续航
   
   👉 请输入要切换的电源模式序号（或 q 退出）：
   ```
## 自动切换电源模式
1. 复制auto-power-mode到/usr/local/bin/auto-power-mode
2. 加可执行权限
```
sudo chmod +x /usr/local/bin/auto-power-mode
```
3. 在启动项中添加auto-power-mode脚本
