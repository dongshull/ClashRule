# ClashRule（自用规则）

## 未经允许请勿随意传播

## 找回Windows的Emoji国旗旗帜图案！Windows修改字体显示Emoji图标！

最近用了几天 Windows，发现在 Window 里面，居然不显示 Emoji 的国旗图案。

如果不显示**国旗图标**只是**国家的简称**未解决之前，所有的软件，以及浏览器中，无法正常显示 Emoji 的国旗标识
在 Clash 中，显示是这样的：
![clash tupian](https://v2rayssr.com/wp-content/uploads/2024/08/a.png)
在 Emoji 大全中，国旗显示这样的：
![clash tupian1](https://v2rayssr.com/wp-content/uploads/2024/08/b.png)

### 问题所在

你电脑的字体缺少EMOJI 图标，导致 Flag 图标显示为 Emoji 的文字。(说人话就是字体不支持)

### 解决方案

#### 下载字体文件
[seguiemj mod ver 1.31](https://github.com/dongshull/ClashRule/main/1.31/seguiemj_mod.ttf)

[seguiemj mod ver 1.33](https://github.com/dongshull/ClashRule/main/1.33/seguiemj_mod.ttf)

1.31 版适用于 Win10 和 Server 2019/2022，1.33 版适用于 Win11。这两个版本的不同之处在 emojipedia (Archive) 上有比较详细的说明。

#### 替换系统字体

使用 `copy` 命令将字体复制到 `%windir%\Fonts` 中。为了更好的兼容性，新字体文件名的 `ASCII` 排序应当在原字体 `seguiemj.ttf` 之前，同时使用 `8.3` 格式。（说人话就是，复制字体文件到 `c:/windows/fonts` 文件夹中，不要更改压缩包里面的字体文件名）

以管理员的身份打开 CMD 窗口，在命令栏中输入以下命令：（修改注册表）

```bash
1. reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts" /v "Segoe UI Emoji (TrueType)" /d segoeemj.ttf /f
```

重启系统使设置生效

#### 大功告成

结局以后，无论是浏览器中，还是系统软件中，久违的 Emoji 国旗图案回来了！

![clash tupian](https://camo.githubusercontent.com/b7b271dacdb992bbb59e270bcb3efe36d8ed50714df2d93039e5ebe096360fd8/68747470733a2f2f76327261797373722e636f6d2f77702d636f6e74656e742f75706c6f6164732f323032342f30382f612e706e67)
![clash tupian](https://v2rayssr.com/wp-content/uploads/2024/08/f.png)
![clash tupian](https://v2rayssr.com/wp-content/uploads/2024/08/d.png)

只是，在 V2rayN 中，不晓得为什么，国旗图案是黑白的！☺

![clash tupian](https://v2rayssr.com/wp-content/uploads/2024/08/ff.png)