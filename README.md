# Mihomo Party ClashRule（自用规则）
[ClashRule](https://raw.githubusercontent.com/dongshull/ClashRule/main/ClashRule.ini)

[My-ClashRule](https://raw.githubusercontent.com/dongshull/ClashRule/main/My-ClashRule.ini)

[My-New-ClashRule](https://raw.githubusercontent.com/dongshull/ClashRule/main/My-New-ClashRule.ini)

[Custom_Clash](https://raw.githubusercontent.com/dongshull/ClashRule/main/Other-rules/Custom_OpenClash_Rules/Custom_Clash.ini)

## 未经允许请勿随意传播

>## [Mihomo Party](https://github.com/mihomo-party-org/mihomo-party/releases)
>![Mihomo Party](https://raw.githubusercontent.com/mihomo-party-org/mihomo-party/refs/heads/master/images/icon-black.png)
>![Mihomo Party1](https://raw.githubusercontent.com/mihomo-party-org/mihomo-party/refs/heads/master/images/preview.jpg)
>## Mihomo Party 常用覆写脚本/示例
>### 使用方法
>1. 复制对应文件 raw 直连，如 `https://raw.githubusercontent.com/dongshull/ClashRule/main/Mihomo-Party/javascript/DongShu%E7%9A%84%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2.js`
`https://raw.githubusercontent.com/dongshull/ClashRule/main/Mihomo-Party/yaml/ACL4SSR_Online_Full_WithIcon.yaml`。
>2. 打开 Mihomo Party，左侧导航栏打开“覆写”页面，粘贴链接后导入，即可看到对应的覆写脚本/配置。
>3. 左侧导航栏打开“订阅管理”，点击需要覆写的订阅右上角的三个点，选择“编辑信息”。
>4. 在打开的对话框中最后一项“覆写”，选择刚刚导入的覆写脚本/配置，保存即可。
#


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

#### 1.下载字体文件
[seguiemj mod ver 1.31](https://github.com/dongshull/ClashRule/main/1.31/seguiemj_mod.ttf)

[seguiemj mod ver 1.33](https://github.com/dongshull/ClashRule/main/1.33/seguiemj_mod.ttf)

`1.31` 版适用于 `Win10` 和 Server 2019/2022，`1.33` 版适用于 `Win11`。这两个版本的不同之处在 `emojipedia (Archive)` 上有比较详细的说明。

#### 2.替换系统字体

使用 `copy` 命令将字体复制到 `%windir%\Fonts` 中。为了更好的兼容性，新字体文件名的 `ASCII` 排序应当在原字体 `seguiemj.ttf` 之前，同时使用 `8.3` 格式。（说人话就是，复制字体文件到 `c:/windows/fonts` 文件夹中，不要更改压缩包里面的字体文件名）

以管理员的身份打开 CMD 窗口，在命令栏中输入以下命令：（修改注册表）

```bash
1. reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts" /v "Segoe UI Emoji (TrueType)" /d segoeemj.ttf /f
```

重启系统使设置生效

#### 3.大功告成

结局以后，无论是浏览器中，还是系统软件中，久违的 Emoji 国旗图案回来了！

![clash tupian](https://camo.githubusercontent.com/b7b271dacdb992bbb59e270bcb3efe36d8ed50714df2d93039e5ebe096360fd8/68747470733a2f2f76327261797373722e636f6d2f77702d636f6e74656e742f75706c6f6164732f323032342f30382f612e706e67)
![clash tupian](https://v2rayssr.com/wp-content/uploads/2024/08/f.png)
![clash tupian](https://v2rayssr.com/wp-content/uploads/2024/08/d.png)

只是，在 V2rayN 中，不晓得为什么，国旗图案是黑白的！☺

![clash tupian](https://v2rayssr.com/wp-content/uploads/2024/08/ff.png)

# Shadowrocket使用说明（IOS Shadowrocket）

```
Shadowrocket快速使用方法：
1.首页 - 添加节点。
2.设置 - 延迟测试方法，选择CONNECT。
3.首页 - 连通性测试，选择可用节点连接。

首次启动会提示【安装VPN配置文件】
请点击【好】和【允许】才能正常使用
```
### 关键词列表
* 首页
   * [添加节点](#添加节点)
   * [添加WireGuard节点](#添加wireguard节点)
   * [更新订阅节点](#更新订阅节点)
   * [节点排序](#节点排序)
   * [SSL错误](#ssl错误)
   * [节点旗帜](#节点旗帜)
   * [节点感叹号](#节点感叹号)
   * [节点分享与整理](#节点分享与整理)
   * [订阅节点筛选](#订阅节点筛选)
   * [代理通过/代理链](#代理通过代理链)
   * [全局路由区别](#全局路由区别)
   * [连通性测试](#连通性测试)
   * [修改测试地址](#修改测试地址)
   * [场景](#场景)
   * [简单模式](#简单模式)
   * [启用回退](#启用回退)
* 配置
    * [配置文件](#配置文件)
    * [扩展配置](#扩展配置)
    * [通用参数](#通用参数)
    * [添加规则](#添加规则)
    * [规则类型](#规则类型)
    * [规则策略](#规则策略)
    * [app分流](#app分流)
    * [更新规则集](#更新规则集)
    * [修改DNS](#修改dns)
    * [no-resolve的作用](#no-resolve的作用)
    * [代理分组/策略组](#代理分组策略组)
    * [代理分组类型](#代理分组类型)
    * [自动切换节点](#自动切换节点)
    * [HTTPS解密](#https解密)
    * [负载均衡](#负载均衡)
    * [模块](#模块)
    * [证书模块](#证书模块)
    * [模块消失](#模块消失)
    * [身份证书密码](#身份证书密码)
    * [微信转圈](#微信转圈)
* 数据
    * [代理日志](#代理日志)
    * [DNS日志](#DNS日志)
    * [iCloud自动同步](#iCloud自动同步)
    * [节点数据管理](#节点数据管理)
    * [流量统计信息](#流量统计信息)
* 设置
    * [延迟测试方法](#延迟测试方法)
    * [小组件](#小组件)
    * [按需求连接](#按需求连接)
    * [VPN自动断开](#vpn自动断开)
    * [前置代理](#前置代理)
    * [代理共享](#代理共享)
    * [检测代理](#检测代理)
    * [代理类型](#代理类型)
    * [开启UDP转发](#开启udp转发)
    * [隐藏VPN图标](#隐藏vpn图标)
    * [GEOIP数据库](#geoip数据库)
* 其他
    * [定位权限](#定位权限)
    * [编译原因](#编译原因)
    * [下载Shadowrocket](#下载shadowrocket)
### 添加节点
* 首页 - 右上角➕ - 类型Subscribe - URL栏输入机场订阅链接 - 保存。

  `订阅链接后面加上#1、#2、#3…，可以重复添加同一个订阅。`

* 首页 - 右上角➕，选择对应节点类型，填写节点配置信息并保存。

  `Shadowrocket已支持的类型：Shadowsocks、ShadowsocksR、Subscribe（订阅）、Vmess、VLESS、Relay、Socks5、Socks5 Over TLS、HTTP、HTTPS、HTTP2、Trojan、Hysteria、Hysteria2、TUIC、Juicity、WireGuard、Snell、Brook、Lua。`

* 复制节点链接，如`trojan://xxx`、`vmess://xxx`、`vless://xxx`等，打开Shadowrocket时会自动识别导入。

* 首页 - 左上角 - 扫码添加。
### 添加WireGuard节点
方法一
* 首页 - 右上角➕ - 类型选择WireGuard，填写配置信息。

方法二
* 复制如下格式的WireGuard配置信息，打开Shadowrocket时会自动弹出“添加对话框”，点击添加。
```
[Interface]
PrivateKey = xxxxxx
Address = 172.16.0.2/32
DNS = 1.1.1.1
MTU = 1420
[Peer]
PublicKey = xxxxxx
AllowedIPs = 0.0.0.0/0
AllowedIPs = ::/0
Endpoint = engage.cloudflareclient.com:2408
Reserved = 12,34,56
```
如果没有自动弹出对话框，可能是因为设置中的`允许检测剪贴板`被关闭了，您可以重新打开，或者点击首页`连通性测试`下方的`粘贴`按钮，手动添加配置信息。
### 更新订阅节点
* 订阅右滑 - 更新。

* 点击首页的更新订阅按钮🔄。

* 设置 - 订阅 - 打开时更新（刷掉后台，重新打开应用程序时会自动更新订阅）。

* 设置 - 订阅 - 自动后台更新（需在系统`设置`-`通用`-`后台App刷新`中开启对Shadowrocket的允许，更新周期为12小时）。

* Shadowrocket提供了「更新订阅」的快捷指令，可以实现自动化操作。

* 长按屏幕的应用图标 - 更新订阅。
```
添加/更新订阅时异常原因：
forbidden 表示订阅被重置或令牌（token）错误。
not found 表示路径信息错误。
service unavailable 表示域名信息错误或域名被运营商屏蔽。
```
### 节点排序
设置 - 订阅 - 根据Ping排序。
### SSL错误
添加/更新订阅链接时，如果提示`发生了SSL错误，无法建立与该服务器的安全连接`，可以尝试的解决方法：
* 全局路由选代理，使用另外一个节点来添加/更新订阅链接。

* 切换网络后再添加/更新订阅链接。

* 检查订阅链接是否错误或失效。
### 节点旗帜
节点优先根据备注名称匹配旗帜，如果匹配不成功，由节点地址解析出IP，通过数据库判断该IP的国家或地区，然后显示对应的旗帜。
* 节点后面ⓘ - 地址栏的图标，可以手动修改旗帜。

* 订阅后面ⓘ - 订阅链接后面ⓘ，利用脚本也能批量修改旗帜。

  `如果把旗帜的Emoji放在节点备注开头，保存时会自动显示对应的旗帜。`
### 节点感叹号
节点显示感叹号原因：

您的节点使用了TLS，地址是IP，却没有设 SNI。

这是错误的，为了可以访问，Shadowrocket会主动开启允许不安全。上一版本`2.2.23`关闭了此功能造成很多人无法使用节点。

`允许不安全`将跳过TLS证书验证，这将导致一些安全问题。如果您使用自签名证书，请将证书导入系统并信任它，否则请及时续订服务器端证书，以防止证书过期。
### 节点分享与整理
节点分享
* 长按节点 - 拷贝，可以把节点链接分享给其他设备。

* 左滑节点 - 二维码，其他设备可以通过扫码添加节点（二维码页面点击右上角的`分享`按钮，可以选择其他形式传送二维码）。

  `节点二维码缺乏统一标准。某些协议（Vmess）的节点，当使用其他代理工具扫码添加时，可能会丢失部分节点信息，导致不能连接。如果遇到此问题，请仔细检查同一个节点的各项配置信息是否一致。`

* 点击节点后面ⓘ，滑动至页面底部，有多种分享节点的菜单。

* 展开节点列表，点击连通性测试下方的编辑按钮`•••`，勾选需要分享的节点，点击左上角的`复制`，可以把多个节点链接同时分享给其他设备。

节点整理
* **调整顺序**：点击编辑按钮`•••`，长按订阅后面的`≡`图标可以调整订阅之间的上下顺序（本地节点默认置顶位置）。

* **节点分类**：非订阅形式添加的节点，默认会归类为`本地节点`。如果需要重新对本地节点进行分类，可以使用`折叠`功能。点击编辑按钮`•••`，勾选节点，点击左上角的`折叠`，为新分类的节点组命名（`折叠`功能可以选择本地节点或者订阅节点）。

* **删除节点**：点击编辑按钮`•••`，点击左上角的`删除`，可以选择删除全部节点或者删除连通性测试结果中的超时节点。

* **滑动菜单**：向右滑动订阅，可以选择`测试`当前订阅节点的连通性，或者`更新`当前订阅节点。向右滑动节点，点击`测试`可以获取单个节点的连通性测试结果，点击`复制`，可以在当前节点列表中新增一个同样配置信息的节点。
### 订阅节点筛选
首页 - 订阅后面ⓘ - 订阅链接后面ⓘ。
* 保留节点名称含有关键词A和B的节点:
```
/(?=.*(A))^(?=.*(B))^.*$/
```
* 保留节点名称含有关键词A或B的节点:
```
A|B
```
* 排除节点名称含有关键词A或B的节点:
```
/^((?!(A|B)).)*$/
```
* 保留节点名称含有关键词A并排除含有关键词B的节点:
```
/(?=.*(A).)^((?!(B)).)*$/
```
分组、代理分组的正则写法与此相同，但需删除前后`/`符号。
### 代理通过/代理链
使用代理链方法：
* **代理通过**：当前代理通过另一个代理转发，支持多级代理。

* 使用节点A连接，点击节点A后面ⓘ，`代理通过`选择节点B，流量走向：`Client` - `B` - `A` - `Web server`
### 全局路由区别
**配置**：流量根据规则进行分配，有些需要通过节点连接，有些则不需要。

**代理**：全部流量都通过同一个节点连接。

**直连**：全部流量都不通过节点连接。

**场景**：根据不同的网络连接类型（Wi-Fi、蜂窝数据）自动切换到预先设置的路由模式，并选择对应的配置文件和节点连接。
### 连通性测试
点击首页的`连通性测试`，节点列表将会显示以毫秒（ms）为单位的延迟数字，这是数据包的传输时间，不同的`延迟测试方法`对应不同的计算结果。长按首页的`连通性测试`，可以临时调整测试方法，仅对本次测试生效。

设置 - 延迟测试方法。
* **TCP**：建立TCP连接的往返时间。

* **ICMP**：发送ICMP回显请求报文和接收ICMP回显应答报文的往返时间。

* **CONNECT**：向测试URL发送一个HTTP HEAD请求，测量从发送请求到接收响应头部信息的往返时间。

  `请优先选择CONNECT，因为它更能准确反映节点的连通性。`

延迟大小与网络上传下载速度没有直接关系，测速请使用其他方法，如：
<https://www.speedtest.net>
### 修改测试地址
用于首页和分组节点的延迟测试
* 首页 - 全局路由 - 分组 - URL测试设置。

用于代理分组节点的延迟测试
* 点击配置文件ⓘ - 代理分组 - 右上角➕ - 最底下URL栏。
### 场景
场景是根据不同的网络连接类型（Wi-Fi、蜂窝数据）自动切换到预先设置的路由模式，并选择对应的配置文件和节点连接。
* 首页 - 全局路由 - 设置的`场景` - 添加场景。

* 为指定的网络连接类型设置对应的路由模式（`配置`、`直连`、`代理`），类型（`节点`、`分组`），`配置文件`，`备注`。

* 网络连接类型分别为：Wi-Fi、蜂窝数据、默认。选择Wi-Fi类型时，SSID需填写Wi-Fi名称。

* 首页 - 全局路由 - 选择`场景`。

首次添加场景，可能会弹出申请权限的对话框，具体原因请看[定位权限](#定位权限)。当没有允许定位权限时，场景列表的☑️标记不会随着网络类型的切换而自动切换，但这不影响场景功能的正常生效。
### 简单模式
首页 - 全局路由 - 分组 - 简单模式。

`简单模式`的功能是自动测试并选择延迟低节点。
* 节点的范围是什么？

> 当开启简单模式，此时下方会出现分组选项，如果没有继续添加分组的操作，节点范围就是首页全部节点，如果添加分组，范围就变成分组里的节点。

* 自动测试的周期是多久？延迟低的判断依据是什么？

> `首页` - `全局路由` - `分组` - `URL测试设置`，这里规定了测试的间隔时间，默认600s，即表示每10分钟自动进行一次节点延迟测试。相邻两次测试结果中最小延迟值的对比，根据公差机制决定是否切换节点，公差越大，触发节点切换的频次越低，默认0ms，即表示只要后面测试结果的最低延迟节点比前面测试结果的最低延迟节点延迟小就会自动切换。

* 切换的节点给什么规则使用？
> Shadowrocket内置策略proxy，简单模式时自动切换的节点使用于所有指向proxy策略的规则。

* 简单模式是自动切换延迟低节点，代理分组的url-test类型也是自动切换延迟低节点，两者有何不同？

> 代理分组创建后，需要在规则中修改策略指向，而简单模式已经关联proxy策略，节省了修改规则的步骤。
> 
> `全局路由`选择`代理`时将导致所有`代理分组`失效，而简单模式依然能够实现自动切换节点。

* 添加分组时，`测速`开关是什么作用？

> 开启测速，这个分组才允许自动切换节点。不开启测速，这个分组只能手动选择节点。
### 启用回退
首页 - 全局路由 - 启用回退。

`启用回退`的功能是当节点连接失败时自动切换其他可用节点。
* 连接失败3次才会触发回退机制。

* 节点只满足可用性，不要求是最低延迟节点。

* 随机切换，不按照节点顺序选择。

* 策略为proxy，节点切换范围就是首页全部节点，如果开启简单模式并选择分组，则范围缩小至分组内节点。

* 策略为分组/代理分组，节点切换范围就是分组或代理分组内节点。

* 具体切换到哪个节点，请查看[代理日志](#代理日志)。
### 配置文件
Shadowrocket内置了一个配置文件`default.conf`，其中包含了国内外网站的分流规则，满足大多数用户的基本需求。此配置文件的内容跟随应用更新而做不定期的调整。如果在使用过程中错误修改或误删配置文件，可以点击`配置` - `恢复默认配置`。

添加配置文件方法：
* 从URL下载配置
  * 配置 - 右上角➕ - 粘贴配置链接 - 下载 - 点击对应的配置文件 - 使用配置。
  * Shadowrocket兼容使用`Clash YAML格式`的配置文件。
 
* 从本地存储或云盘导入
  * 配置 - 从云导入，点击对应存储路径的配置文件。

点击配置文件，显示操作菜单：
* 使用配置
* 编辑纯文本
* 更新配置
* [扩展配置](#扩展配置)
* 重新命名
* 导出

点击配置文件的ⓘ图标，进入编辑菜单：
* [通用](#通用参数)
* [规则](#添加规则)
* Hosts
* URL重写
* HTTPS解密
* 脚本
* 代理分组
* 脚本URL
* 规则集URL
* 复制
* 替换策略
* 测试规则

配置文件的纯文本编写方法，请参考：
* [懒人配置](https://raw.githubusercontent.com/wlxuf/Shadowrocket/main/lazy.conf)

* [懒人配置（含策略组）](https://raw.githubusercontent.com/wlxuf/Shadowrocket/main/lazy_group.conf)
### 扩展配置
* 从配置a扩展出配置b，此时默认关系是b包含a，也可以理解为b继承了a的内容。

* 配置b优先级高于配置a，该功能是对配置建立包含关系，以满足同时使用多个配置的需求。

* 点击配置文件ⓘ - 通用 - 包含配置，可以修改或解除包含关系。
### 通用参数
**旁路系统（bypass-system）**：如果禁用此选项，可能会导致一些系统问题，如推送通知延迟。

**跳过代理（skip-proxy）**：此选项强制域名或IP的连接范围由Shadowrocket TUN接口来处理，而不是Shadowrocket代理服务器。此选项用于解决一些应用程序的一些兼容性问题。

**TUN旁路路由（tun-excluded-routes）**：Shadowrocket TUN接口只能处理TCP协议。使用此选项可以绕过指定的IP范围，让其他协议通过。

**DNS覆写（dns-server）**：使用普通DNS或加密DNS（如doh、doq、dot等）覆盖默认的系统DNS。有些dns over https支持http3，所以尝试查询，如果支持就切换到http3，可在doh链接后面加上`#no-h3`关闭。doh强制通过h3查询的写法是将`https`改成`h3`，如`h3://dns.alidns.com/dns-query`。

**备用DNS（fallback-dns-server）**：当覆写DNS查询失败或查询时间超过2秒，Shadowrocket会自动回退备用DNS。如需指定多个DNS，可用逗号分隔。system表示回退到系统DNS。

**启用IPv6支持（ipv6）**：false表示不启用，true表示启用。即使不启用此选项，当本地网络环境支持IPv6，并且节点域名支持IPv6解析，Shadowrocket也会使用节点的IPv6地址进行访问。解决方法是关闭节点域名的IPv6解析，或者在配置文件的`[Host]`项目下为节点域名指定IP地址。

**首选IPv6（prefer-ipv6）**：优先向IPv6的DNS服务器查询AAAA记录，优先使用AAAA记录。false表示不启用。

💡 **dns-direct-system**：直连的域名类规则使用系统dns进行查询。false表示不启用。

💡 **icmp-auto-reply**：ping数据包自动回复。

💡 **always-reject-url-rewrite**：不开启时，「重写的REJECT策略」默认只有在配置模式下生效。开启后，可以令该策略在其他全局路由模式下都生效。

**私有IP应答（private-ip-answer）**：如果不启用该选项，域名解析返回私有IP，Shadowrocket会认为该域名被劫持而强制使用代理。

💡 **dns-direct-fallback-proxy**：直连域名解析失败后使用代理。false表示不启用。

**TUN包含路由（tun-included-routes）**：默认情况下，Shadowrocket接口会声明自己为默认路由，但由于Wi-Fi接口的路由较小，有些流量可能不会通过Shadowrocket接口。使用此选项可以添加一个较小的路由表。

**总是真实IP（always-real-ip）**：这个选项要求Shadowrocket在TUN处理DNS请求时返回一个真实的IP地址而不是假的IP地址。

**DNS劫持（hijack-dns）**：有些设备或软件总是使用硬编码的DNS服务器，例如Netflix通过Google DNS(`8.8.8.8`或`8.8.4.4`)发送请求，您可以使用此选项来劫持查询。

💡 **udp-policy-not-supported-behaviour**：当UDP流量匹配到规则里不支持UDP转发的节点策略时重新选择回退行为，可选行为包括DIRECT、REJECT。DIRECT表示直连转发UDP流量，REJECT表示拒绝转发UDP流量。

**包含配置（include）**：表示当前配置包含另一个配置的内容，当前配置的优先级高于被包含配置。该选项是对配置建立包含关系，以满足同时使用多个配置的需求。

`带💡符号的参数只能通过配置文件的纯文本模式进行设置，没有UI操作选项。`
### 添加规则
* 点击配置文件ⓘ - 规则 - 右上角➕，根据需求选择[规则类型](#规则类型)和[规则策略](#规则策略)，填写规则内容。

* 数据 - 代理 - 启用日志记录，产生网络活动后回到该页面，从最近的日志中查看网络活动记录，点击任一记录查看详情，点击右上角`•••`选择类型添加规则。

* 规则匹配的优先级：
  * 上面规则优先于下面规则。
  * 域名规则优先于IP规则。
### 规则类型
**DOMAIN-SUFFIX**：匹配请求域名的后缀。

如`DOMAIN-SUFFIX,example.com,DIRECT`可以匹配到`a.example.com`、`a.b.example.com`。

**DOMAIN-KEYWORD**：匹配请求域名的关键词。

如`DOMAIN-KEYWORD,exa,DIRECT`可以匹配到`a.example.com`、`a.b.example.com`。

**DOMAIN**：匹配请求的完整域名。

如`DOMAIN,www.example.com,DIRECT`只能匹配到`www.example.com`。

**USER-AGENT**：匹配用户代理字符串，支持使用通配符`*`。

如`USER-AGENT,MicroMessenger*,DIRECT`可以匹配到`MicroMessenger Client`。

**URL-REGEX**：匹配URL正则式。

如`URL-REGEX,^https?://.+/item.+,REJECT`可以匹配到`https://www.example.com/item/abc/123`。

**IP-CIDR**：匹配IPv4或IPv6地址。

如`IP-CIDR,192.168.1.0/24,DIRECT`可以匹配到IP段`192.168.1.1～192.168.1.254`。当域名请求遇到IP类规则时，Shadowrocket会向本地DNS服务器发送查询请求，以判断主机IP是否匹配规则。若IP类规则加`no-resolve`(如：`IP-CIDR,172.16.0.0/12,DIRECT,no-resolve`)，则域名请求将会跳过此规则，不会触发本地DNS查询。

**IP-ASN**：匹配IP地址隶属的ASN编号。

如`IP-ASN,56040,DIRECT`可以匹配到属于China Mobile Communications Corporation网络的IP地址。

**RULE-SET**：匹配规则集内容。规则集的组成部分需包含规则类型。

**DOMAIN-SET**：匹配域名集内容。域名集的组成部分不包含规则类型。

**SCRIPT**：匹配脚本名称。

**DST-PORT**：匹配目标主机名的端口号。

如`DST-PORT,443,DIRECT`可以匹配到443目标端口。
  
**GEOIP**：匹配IP数据库。

如`GEOIP,CN,DIRECT`可以匹配到归属地为CN的IP地址。

**FINAL**：兜底策略。

如`FINAL,PROXY`表示当其他所有规则都匹配不到时才使用FINAL规则的策略。

**AND**：逻辑规则，与规则。

如`AND,((DOMAIN,www.example.com),(DST-PORT,123)),DIRECT`可以匹配到`www.example.com:123`。

**NOT**：逻辑规则，非规则。

如`NOT,((DST-PORT,123)),DIRECT`可以匹配到除了`123`端口的其他所有请求。

**OR**：逻辑规则，或规则。

如`OR,((DST-PORT,123),(DST-PORT,456)),DIRECT`可以匹配到`123`或`456`端口的所有请求。

**PROTOCOL**：匹配传输协议类型。

`PROTOCOL`类型不支持单独使用，只能作为子规则类型嵌套于逻辑规则当中。如`AND,((PROTOCOL,UDP),(DST-PORT,443)),REJECT-NO-DROP`。
### 规则策略
**PROXY**：代理。通过代理服务器转发流量。

**DIRECT**：直连。连接不经过任何代理服务器。

**REJECT**：拒绝。返回HTTP状态码404，没有内容。

**REJECT-DICT**：拒绝。返回HTTP状态码200，内容为空的JSON对象。

**REJECT-ARRAY**：拒绝。返回HTTP状态码200，内容为空的JSON数组。

**REJECT-200**：拒绝。返回HTTP状态码200，没有内容。

**REJECT-IMG**：拒绝。返回HTTP状态码200，内容为1像素GIF。

**REJECT-TINYGIF**：拒绝。返回HTTP状态码200，内容为1像素GIF。

**REJECT-DROP**：拒绝。丢弃IP包。

**REJECT-NO-DROP**：拒绝。返回ICMP端口不可达。

除此之外，规则策略还可以选择`代理分组`、`订阅名称`、`分组`、`服务器节点`。
### app分流
根据不同app指定分流规则的方法。

示例：YouTube app 分流走代理。

* 复制YouTube的规则集链接
```
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Shadowrocket/YouTube/YouTube.list
```
* 点击配置文件ⓘ - 规则 - 右上角➕，类型选择`RULE-SET`，策略选择`PROXY`，输入框内粘贴“规则集链接”，保存完成（策略可以根据需求使用其他选项）。

iOS系统没有常规分应用代理的操作，只能通过`域名` / `ip` / `ua`规则实现app分流效果。可自行抓包，或者订阅[blackmatrix7](https://github.com/blackmatrix7)的[规则集](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Shadowrocket)。如果引用的链接是域名集，添加规则时，类型请选择`DOMAIN-SET`。
### 更新规则集
点击配置文件 - 使用配置。
### 修改DNS
* 点击配置文件ⓘ - 通用 - DNS覆写，删除`system`，添加 `223.5.5.5,119.29.29.29`。也可以使用加密DNS，如`DNS-over-TLS`、`DNS-over-HTTPS`、`DNS-over-QUIC`。

* **备用DNS**：当覆写的DNS查询失败后回退备用DNS进行查询。如需指定多个DNS，可用逗号分隔。`system`表示回退到系统DNS。
### no-resolve的作用
* 当域名请求遇到IP类规则时，Shadowrocket会向本地DNS服务器发送查询请求，以判断主机IP是否匹配规则。

* 若IP类规则加`no-resolve`，则域名请求将会跳过此规则，不触发本地DNS查询。如：
```
IP-CIDR,172.16.0.0/12,DIRECT,no-resolve
```
### 代理分组/策略组
* 点击配置文件ⓘ - 代理分组 - 右上角➕。填写名称，根据需求选择类型，通过`正则`匹配策略，或者从策略输入框后面的`•••`手动添加策略，保存。

* 策略是规则的组成部分，创建的代理分组只有放到规则里才能发挥作用。
进入对应规则的详情页，点击策略选项，从列表中选择代理分组，保存。

* 首页下拉，可以快捷进入代理分组界面。
### 代理分组类型
**select**：手动切换节点。

**url-test**：自动切换延迟最低节点。

**fallback**：节点挂掉时自动切换其他可用节点。

**load-balance**：不同规则的请求使用分组里的不同节点进行连接，相同的域名会使用同一个节点。

**random**：随机使用分组里的不同节点进行连接。
### 自动切换节点
自动切换延迟低的节点：

方法一
* 首页 - 全局路由 - 分组 - 简单模式 - 打开。

方法二
* 点击配置文件ⓘ - 代理分组 - 右上角➕ - 类型`url-test`。
### HTTPS解密
打开HTTPS解密方法：
* 点击配置文件ⓘ - HTTPS解密 - 证书 - 生成新的CA证书 - 安装证书。

* 系统设置 - 已下载描述文件 - 安装。

* 系统设置 - 通用 - 关于本机 - 证书信任设置 - 开启对应Shadowrocket证书信任。
### 负载均衡
使用负载均衡策略类型方法：

点击配置文件ⓘ - 代理分组 - 右上角➕，类型选择`load-balance`。

「load-balance」表示不同规则的请求使用分组里的不同节点进行连接，相同的域名会使用同一个节点。
### 模块
添加模块方法:

本地新建模块
* 模块跟配置的语法相同。您可以在模块里调整通用设置以及添加规则、Hosts、重写、脚本、证书内容、解密主机名。

下载远程模块
* 模块 - 右上角➕ - 填写模块链接 - 下载。
* 模块 `[MITM]` 部分写法：
```
hostname = %APPEND% 主机名
```
* 加 `%APPEND%` 表示把内容插入到配置中，不加时会覆盖配置中对应内容，并影响其他模块功能。

请对正在使用的配置开启HTTPS解密，模块才能完整生效。
### 证书模块
切换配置文件时免除重复安装CA证书方法：

* 点击「已安装证书的配置文件」后面ⓘ - HTTPS解密 - 证书后面ⓘ - 复制。

* 新建模块：
```
#!name=证书（名字可更改）
[MITM]
enable=true
ca-passphrase=证书密码（即「已安装证书的配置文件」的证书密码，默认密码是Shadowrocket）
ca-p12=证书内容（即剪贴板复制的内容）
```
原本是可以省略`ca-passphrase`这行参数。但由于引用的配置文件可能已经包含了证书密码，且证书密码可能不是`Shadowrocket`，为防止出错，因此才增加`ca-passphrase`参数来覆盖引用的配置文件的证书密码。
### 模块消失
模块页面已经开启`保存到iCloud`，如果出现模块消失的问题，请检查：

* 系统设置 - Apple ID - iCloud - 使用iCloud的APP中，确保Shadowrocket/iCloud云盘已经打开同步。

* 文件app - iCloud云盘 - Shadowrocket，确定其中包含`Modules`和`Script`两个子文件夹。

* 文件app - iCloud云盘 - Shadowrocket - Modules，如果iCloud的本地缓存被清理，此时模块文件是未下载状态，请等待自动下载或手动下载。
### 身份证书密码
Shadowrocket安装CA证书时，如果遇到「输入证书`身份证书`的密码」页面，可以尝试输入：`Shadowrocket`
### 微信转圈
如果使用Shadowrocket时微信一直显示`连接中/收取中`，可以尝试的解决方法：
* 微信分流走直连。

* 点击配置文件ⓘ - 通用 - 启用IPv6 - 关闭。
### 代理日志
`代理日志`记录了网络活动过程中Shadowrocket处理请求的具体信息。
* 数据 - 代理 - 启用日志记录。

* 产生网络活动时，返回`数据` - `代理`页面查看日志文件。

* 每条记录包含信息：
    * 请求URL
    * 请求匹配的规则策略
    * 请求传输协议
    * 请求发送时间

* 记录显示`MITM`，表示请求域名已启用解密。

* 点击每条记录查看详情，详情页右上角`•••`可以选择类型添加规则。

* `数据` - `代理`页面，右上角`•••`可以手动删除所有日志文件。日志文件页面，右上角`•••`可以选择导出。

  `数据 - 自动删除 - 打开，程序会自动删除7天前的日志文件。Shadowrocket已连接状态，手动删除将保留最新的日志文件，未连接时，手动删除所有。`
### DNS日志
`DNS日志`记录了网络活动过程中DNS服务器处理域名查询请求的具体信息。
* 数据 - 代理 - DNS - 启用日志记录。

* 产生网络活动时，返回`数据` - `DNS`页面查看日志文件。

* 每条记录包含信息：
    * 请求域名
    * 查询结果
    * DNS响应时间
    * 处理请求的DNS

* 旗帜是根据返回IP地址的地理位置信息自动显示。

* `覆写DNS`不可用或未返回有效响应时，回退`备用DNS`来查询域名。

  `记录信息中如果响应时间超过2秒，意味着系统正在触发回退机制。`
### iCloud自动同步
Shadowrocket支持将服务器节点、配置文件、模块和脚本文件等数据类型自动同步至iCloud云端。
* 数据 - iCloud - 自动同步 - 打开。

* 设备`设置` - `账号` - `iCloud`，确保使用iCloud的APP列表中已经开启`Shadowrocket`和`iCloud云盘`项目，否则会出现`iCloud自动同步失败`的提示。

* 同步成功时，点击`iCloud文件`可以看到存储云端的配置文件。

* `文件app` - `iCloud云盘` - `Shadowrocket`，可以看到存储云端的所有数据。其中的`shadowrocket.v2.model`文件包含服务器节点的配置信息。

* iCloud服务中断、网络连接问题以及其他复杂原因可能导致iCloud同步异常，这种情况建议选择手动删除iCloud备份并重新同步数据。

  `如果用户删除首页某个节点后发现它又自动恢复，可以尝试以下解决方法：数据 - iCloud，服务器节点下面点击删除iCloud备份和同步服务器节点。`

* 添加的`场景`和`分组`不属于iCloud自动同步的数据类型，需要手动备份下载，才能在设备间共享数据。
### 节点数据管理
**导出节点**：将首页的所有节点数据整合成一个JSON文件，选择存储在本地或云端，也可以通过其他共享方式传输文件。

**导入节点**：将存储在本地或云端JSON文件中的节点数据解析并添加到首页。

**删除本地节点**：一键删除首页所有节点数据。
### 流量统计信息
`统计`是Shadowrocket开启连接后接管设备所有网络传输的流量统计信息。
* 数据 - 统计。

* 统计包含信息：
    * 开始时间
    * 连接时间
    * Wi-Fi和蜂窝数据的上下行流量
    * 流量分流的柱形图统计

* 默认记录所有流量统计信息。打开`启用存档`将会单独记录每一次连接的流量统计信息，关闭首页连接后可以从`归档`查看。

* 点击右上角`•••`可以重置统计信息。

首页`订阅`支持显示流量统计信息。方法是在订阅链接指向的纯文本base64编码前添加`STATUS=xxx`或`REMARKS=xxx`字段，这样订阅名称下方就能显示自定义信息。如果没有添加字段或者[隐藏用户代理字符串](#隐藏用户代理字符串)，可能导致不返回相关统计信息，只显示时间。
### 延迟测试方法
详见词条[连通性测试](#连通性测试)
### 小组件
* 设置 - 小组件。

* **服务器节点**：根据需求添加6个常用节点，点击Today小组件右上角的`>`可以展开查看，方便手动切换节点。

* **显示Ping值**：启用后，长按Today小组件中心位置可以测试`服务器节点`连通性并显示延迟数字。

* **根据Ping排序**：启用后，长按Today小组件中心位置可以测试`服务器节点`连通性并依延迟大小自动排序。

添加小组件方法：

Today小组件

* 负一屏 - 编辑 - 自定 - 点击Shadowrocket旁边的“添加”按钮 ➕。

屏幕小组件

* 长按屏幕 - 左上角➕ - Shadowrocket，选择合适类型添加。（系统要求≥ iOS 17）

更新Shadowrocket后，如果找不到小组件添加按钮，请尝试重启手机。如果小组件显示“无法加载”，请尝试以下方法：

* 系统设置 - 通用 - 语言与地区，添加或删除一种其他语言。
### 按需求连接
**始终开启**
* VPN保持连接状态。意外断开或者重启设备，也会自动连接。

* 通过应用`首页`临时关闭连接。设备设置中的VPN状态以及小组件开关不能直接关闭。

* `脚本`/`模块`/`解密`等需求比较多时建议开启。

**按需求连接**
* 根据添加的`按需求规则`自动切换VPN状态。默认规则是任意网络类型下保持连接状态，相当于`始终开启`。

* 按需求规则：
    * 当访问列表中的`域名`时，系统会向Shadowrocket发送请求，如果响应成功，VPN自动连接。
    * 网络中指定的`DNS`（通常认为是网络运营商/Wi-Fi路由器提供的DNS服务器地址）与列表任一内容相匹配时，VPN自动连接或断开。
    * `SSIDS`填写需要匹配的Wi-Fi名称。
    * VPN连接行为可以通过`网络类型`/`域名`/`DNS`条件触发。
    * VPN断开行为不能通过`域名`条件触发。
    * 从上到下依次匹配添加的`按需求规则`。
- 添加`按需求规则`后，打开`按需求连接`开关，规则才能生效。

* 同时打开`始终开启`和`按需求连接`，只有`始终开启`选项能够生效。
  
**睡眠时断开**
* 当设备进入睡眠状态，VPN自动断开连接。

* Shadowrocket响应系统发送的睡眠指令才会断开连接，有时候熄屏的系统未必处于睡眠状态。

**显示断开信息**
* 显示VPN断开连接的通知信息。
### VPN自动断开
系统版本低于`iOS 15`、处理复杂请求、加解密数据、运行脚本等因素相互作用之下可能导致NE内存占用过高，从而造成VPN自动断开，解决方法：

`设置` - `按需求连接` - 打开 `始终开启`。
### 前置代理
设置 - 代理 - 前置代理。

「前置代理」表示所有流量先通过HTTP/SOCKS5代理转发，再根据配置规则向节点服务器发送请求。
### 代理共享
局域网条件下

* A设备：设置 - 代理 - 代理共享 - 启用共享。

* B设备：系统设置 - WiFi - WiFi名称后面ⓘ - HTTP代理 - 手动输入Shadowrocket「代理共享」的IP和端口。

使用热点条件下

* A设备：开启热点。

* B设备：连接热点。

* 然后按照局域网条件下方法进行设置。
### 检测代理
如果在使用 Shadowrocket 的时候，遇到某些 APP 提示需关闭代理才能使用，可以在 `Shadowrocket` - `设置` - `代理类型` - 选择 `None`。
### 代理类型
Shadowrocket代理类型：

* 设置 - 代理 - 代理类型。

* **HTTP**：系统代理模式，对于不支持的程序会交给tun接管网络连接。

* **None**：tun模式，全部网络请求都将通过tun接口进行处理。
### 开启UDP转发
* 设置 - UDP - 开启转发- 打开。

* 首页 - 订阅后面ⓘ - UDP转发 - 打开。

* 首页 - 节点后面ⓘ - UDP转发 - 打开。
### 隐藏VPN图标
设置 - 排除路由0.0.0.0/31 - 打开。
### GEOIP数据库
设置 - GeoLite2数据库。

方法一
* 填写[MaxMind官网](https://www.maxmind.com)注册的账户ID和密钥，点击下方的`更新`按钮。

方法二
* 关注GitHub的IP数据库项目，复制mmdb格式的下载链接，粘贴在国家/ASN对应的URL位置，点击`更新`按钮。当点击`重置`时，可以恢复为系统自带的数据库。

[Loyalsoldier](https://github.com/Loyalsoldier/geoip)的IP数据库：
```
https://raw.githubusercontent.com/Loyalsoldier/geoip/release/Country.mmdb
```
[Hackl0us](https://github.com/Hackl0us/GeoIP2-CN)的IP数据库：
```
https://github.com/Hackl0us/GeoIP2-CN/raw/release/Country.mmdb
```
Masaiki的IP数据库：
```
https://github.com/Masaiki/GeoIP2-CN/raw/release/Country.mmdb
```
[P3TERX](https://github.com/P3TERX/GeoLite.mmdb)的ASN数据库：
```
https://github.com/P3TERX/GeoLite.mmdb/raw/download/GeoLite2-ASN.mmdb
```
### 定位权限
* iOS系统的要求，开启定位权限才能获取Wi-Fi名称。

* 如果不需要在Shadowrocket里看到Wi-Fi信息，那么就可以不用开启。
### 编译原因
Shadowrocket2.2.29之前的版本是使用Xcode 13.2.1编译的。

2023年4月份以后，苹果官方要求开发者在提交应用到App Store时必须至少使用Xcode 14编译，所以iOS12以下系统无法使用。

Shadowrocket下一个版本`2.2.30`将设置最低安装要求iOS12，然后停止`2.2.29`版本，iOS低版本用户就可以方便安装`2.2.28`版本。
### 下载Shadowrocket
Shadowrocket只有iOS/iPadOS/tvOS版本和M系列芯片的Mac才能下载，开发者是`Shadow Launch Technology Limited`。**Shadowrocket没有安卓/Windows版本！**

下载方法：
* 非国区ID登陆App Store，搜索`Shadowrocket`，购买后下载。

* Shadowrocket是买断制的付费软件。

* 美区价格：2.99美元。

* 使用美区ID时，地址建议填免税州。
```
五个免税州：
俄勒冈州（Oregon）
蒙大拿州（Montana）
特拉华州（Delaware）
新罕布什尔州（New Hampshire）
阿拉斯加州（Alaska）部分区域
```
[美国地址生成器](https://www.meiguodizhi.com)

[美区Apple ID注册方法](https://blog.skylershu.com/post/apple-id-us-2022)

[Apple官网购买礼品卡方法](https://blog.skylershu.com/post/apple-gift-card)

[Shadowrocket下载链接](https://apps.apple.com/app/shadowrocket/id932747118)