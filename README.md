1、 适用于Debian/Ubuntu/Mint
2、 将power-mode-set文件复制到/usr/local/bin, 然后sudo chmode +x power-mode-set
3、 可在菜单目录添加一个【电源模式】菜单，例如：linux mint xfce下
可在~/.local/share/applications下添加一个菜单项
可以vim ~/.local/share/applications/power-mode.desktop，并粘贴以下内容
```
[Desktop Entry]
Name=电源模式
Comment=切换电源性能模式
Exec=xfce4-terminal --title="电源模式切换" --hold -e "/usr/local/bin/power-mode-set"
Icon=preferences-system-power
Terminal=false
Type=Application
Categories=System;

```
就可以在菜单中找到这个菜单了
