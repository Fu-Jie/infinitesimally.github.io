---
# layout    : archive
title     : sublime_text 配置技巧
date      : 2018-10-01 21:30:05
categories: Sublime_Text
classes   : wide
# permalink : /PowerShell/
---
这里记录一些有关sublimetxt使用的一些技巧，做个备忘。

## sublimetext的程序菜单选项分别由一下文件组成。
    + Main.sublime-menu (也就是主菜单选项，通过修改这个文件可以修改主菜单的选项名等。)
    + Side Bar.sublime-menu (侧边栏右键菜单，同样可以修改选项名)
    + Context.sublime-menu (文本编辑窗口右键菜单)

## 修改首选项插件设置行为，使打开设置为默认和用户分屏效果.

+ json格式

```json
{
    "command": "edit_settings",
    "args":
    {
        // 根据插件的名字来修改下面2个路径的名字，一个是插件默认设置的安装位置，一个是用户安装位置。
        "base_file": "${packages}/SideBarEnhancements/Side Bar.sublime-settings",
        "default": "${packages}/User/Side Bar.sublime-settings"
    },
    "caption": "Settings"
},
```

+ 设置的xml代码片段

```xml
<!-- ${packages}需要转义！ -->
<snippet>
    <content><![CDATA[
{
    "command": "edit_settings",
    "caption": "设置",
    "args":
    {
        "base_file": "\$\{packages\}/${1:package_name}/${1:package_name}.sublime-settings",
        "default": "// Settings in here override those in \"${1:package_name}/${1:package_name}.sublime-settings\",\n// and are overridden in turn by syntax-specific settings.\n{\n\t$0\n}\n"
    },
},
]]></content>
    <tabTrigger>st</tabTrigger>
    <scope>source.json</scope>
</snippet>
```



