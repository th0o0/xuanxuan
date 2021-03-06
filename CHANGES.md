# 更新记录

## v 1.1.1

[2017-05-05]

本次更新集成了然之的签到功能，对客户端界面进行了大量交互细节优化，并且处理社区反馈的大量问题。现在最新发布的然之 4.2.2 已内置喧喧最新版本，大家无需在为然之安装扩展。喧喧还启用了全新的域名 [xuan.im](http://xuan.im)，欢迎大家访问网站了解更多内容。

### 更新明细：

* **客户端**：
  + 增加用户个人配置云同步功能，在登录时会从服务器获取客户端配置，退出时上传个人配置到服务器；
  + 现在会记住用户上次保存文件的位置，在打开保存位置对话框时会自动定位到用户上次保存的位置；
  + 在上传文件之前会先检查服务器设置的最大允许上传文件大小，如果不符合要求会提示用户并拒绝上传文件；
  + 修复上传或下载文件服务器提示错误没有捕捉到的问题；
  + 用户当天第一次登录时会提示签到成功的消息；
  + 更改导航上项目顺序，现在讨论组排在联系人上方；
  + 最近会话不再是可选的（已经从设置面板中移除设置），首次启动时会默认显示最近会话；
  + 当最近会话没有中导航上激活时，如果当前会话收到消息或着向外发送了消息会自动激活最近会话；
  + 当激活一个包含新消息的会话时会自动滚动到消息列表的底部（如果在之前滚动位置发生过变化）；
  + 优化导航下拉菜单界面，去掉“离线”条目，增加“注销”条目；
  + 优化会话和联系人搜索功能，现在当在联系人列表时只会在联系人会话中查找，当在讨论组列表时只在讨论组中查找，最近会话列表中可以查找所有会话；
  + 修复第一次使用时没有在导航上定位到最近会话的问题；
  + 调整了系统会话在讨论组列表上的显示顺序，现在系统会话会显示在除加星会话的上方；
  + 优化了会话底部工具栏上的图标外观，增加更改字体大小图标按钮，点击按钮会弹出面板来实时更改字体大小，更改会话字体大小功能不再在会话下拉菜单中提供访问入口；
  + 调整了默认会话字体设置，现在文字的行间距更适合阅读；
  + 现在在消息发送框“@他人”时，默认显示用户真实姓名；
  + 修复无法显示消息中的空白行的问题；
  + 修复有用户推出讨论组时，讨论组消息短暂消失的问题；
  + 会话侧边栏文件列表中不再显示发送失败的文件，移除了文件列表中的图标，修复了有时文件名无法显示完整的问题，修复了文件列表无法自动更新的问题；
  + 修复了会话侧边栏上的成员列表在有用户退出时没有正确刷新的问题，修复了一对一会话也显示管理员标志的问题；
  + 调整会话侧边栏最小宽度；
  + 现在请求退出应用时（点击关闭按钮或者在通知栏图标上选择退出），会立即关闭主界面而不是先显示登录界面再退出；
  + 当服务器连接超时时，会在客户端上显示提示消息；
  + 优化新建会话对话框中联系人排列顺序；
  + 优化 Windows 上用户个人设置对话框操作按钮显示顺序；
  + 优化在 Windows 上任务栏高亮闪烁提示功能，现在会一直高亮，直到窗口被激活；
  + 优化关于对话框上的内容显示；
  + 优化界面上工具提示显示的动画效果；
  + 优化了界面上的文本，更符合语义；
  + 开发支持：
    - 修复了第一次启动调试时等待时间过长的问题，移除了首次运行自动安装 React 扩展策略；
* **xxd 服务器**
  + 增加了xxd到然之服务器和客户端的通信容错处理；
  + 增加了默认然之服务器的设置，客户端登录不填写服务器名称时xxd使用默认设置；
  + 增加了限制附件上传大小的配置；
* **然之服务器**
  + 加解密功能优先使用 `openssl` 扩展，其次选择 `mcrypt` 扩展，两者都未启用时使用内置纯 PHP 实现的 AES 加密类库；
  + 喧喧登录和然之签到集成，可以在然之中设置只能通过喧喧签到；
  + 然之内置对喧喧 1.1.1 的支持，现在使用最新版然之（4.2.2+）不再需要为然之安装喧喧扩展包；
  + 修复新系统安装后没有系统会话（包含系统所有成员的讨论组）的问题；
  + 然之升级时检测喧喧版本，并自动升级喧喧；
  + 可以在然之后台设置和xxd通信需要的密钥；
* **网站和文档**
  + 网站启用全新域名：[http://xuan.im](http://xuan.im)；
  + 文档进行了更新。

### 下载地址：

* Windows 7+：[64 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-win64-setup.exe)、[64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-win64-zip.exe)、[32 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-win32-setup.exe)、[32 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-win32-zip.exe)、[64 位 Debug 安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-debug-win64-setup.exe)
* MacOS：[xuanxuan-1.1.1-mac.dmg](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-mac.dmg)
* Linux：[64 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-linux-x64.tar.gz)、[64 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-linux-amd64.deb)、[64 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-linux-x64.rpm)、[32 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-linux-ia32.tar.gz)、[32 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-linux-i386.deb)、[32 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.1-linux-ia32.rpm)
* Server: [windows 64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.1-win64.zip)、[windows 32 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.1-win32.zip)、[mac 压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.1-mac.tar.gz)、[linux 64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.1-linux-x64.tar.gz)、[linux 32 位 压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.1-linux-ia32.tar.gz)；
* 然之：[源码包](http://dl.cnezsoft.com/ranzhi/4.2.2/ranzhi.4.2.2.zip)、[windows 一键安装包](http://dl.cnezsoft.com/ranzhi/4.2.2/ranzhi.4.2.2.exe)、[linux rpm 安装包](http://dl.cnezsoft.com/ranzhi/4.2.2/ranzhi-4.2.2-1.noarch.rpm)、[linux deb 安装包](http://dl.cnezsoft.com/ranzhi/4.2.2/ranzhi_4.2.2_1_all.deb)。

## v 1.1.0

[2017-04-28]

本次更新大幅改进客户端界面交互体验，增加会话和联系人搜索功能，优化表情显示，增加个人设置面板，轻松定制消息提醒方式和窗口界面行为。

服务器进行了重大改进：增加全新的 go 语言实现的服务器（xxd），全程使用 AES 加密消息，通过 WebSocket 和 https 与客户端通信，使用 http 或 https 与然之服务器或你的网站进行通信。重构了然之服务器（现在然之服务器仅提供 http 接口）。客户端仍然支持 1.0 版的服务器，需要在登录框填写服务器地址时添加 `#v1.0` 后缀。

### 更新明细：

* **客户端**：
  - 重构了导航布局，现在头像默认在下方显示（可以在个人设置中更改），去掉了导航折叠和展开功能，原会话和通讯录标签改为最近聊天（最近聊天可以在个人设置中关闭）、联系人和讨论组；
  - 全新的会话列表功能，可以按照最近聊天、联系人和讨论组分别查看对应的会话，原通讯录功能已合并到联系人会话列表，优化了会话列表界面，现在更易于区分收藏的会话或离线联系人会话，公开频道现在更名为公开讨论组；
  - 增加会话搜索功能，并支持使用用户联系方式、拼音全拼或简拼进行搜索；
  - 增加个人设置功能，可以在用户头像下拉菜单中打开个人设置面板，方便用户个性化聊天、通知、导航、窗口及快捷键等多个设置选项；
  - 优化所以对话框中操作按钮的显示顺序，现在会根据运行平台使用符合用户操作系统习惯的顺序显示；
  - 重构了表情选择面板，现在能够选择全部 Emoji 表情😄，并支持搜索表情（需要中个人设置中开启表情搜索功能），表情符图片资源已升级到 Emoji one 3.0；
  - 新建讨论组时会提示为讨论组设置名称；
  - 会话侧边栏现在支持通过拖拽边缘来调整宽度，并且会自动保存侧边栏状态到用户配置；
  - 讨论组会话会在初始状态下自动显示侧边栏；
  - 优化侧边栏上的用户列表显示顺序，现在优先显示管理员用户和在线用户；
  - 消息发送框中的表情快捷代码会自动转换显示为表情符😊，如果消息发送框中只包含一个表情符会自动使用高清表情图片发送（可以在个人设置中关闭），在消息框中输入的所有 emoji unicode 字符会中发送之前自动转换为快捷代码以防止服务器不支持特殊字符；
  - 消息发送框中输入 @用户 会自动高亮显示用户名称并支持点击查看用户资料；
  - 优化会话消息列表界面，高亮显示提到（@me）自己的字符，消息中的表情符边缘会更加突出易于辨认，现在复制消息列表中的消息不会中复制的内容中包含时间文本；
  - 现在全局截图后会将图片放置在剪切版；
  - 现在允许关闭消息框小技巧提示按钮（可以在个人设置中重新开启）；
  - 点击侧边栏用户列表上的用户默认操作为在消息发送框中 @此用户；
  - 优化消息中包含一级或二级标题格式文本的显示，现在会以更易于阅读的样式显示；
  - 修复了中消息中以代码发送 `<`、 `>` 会被转码的问题；
  - 优化了消息中的代码显示样式；
  - 修复在 Windows 上复制消息并粘贴到消息发送框自动在首尾添加空格的问题；
  - 修复会话消息历史记录中链接点击出现界面空白的问题；
  - 修复新建会话时查找公开会话失败的问题（issue #6）；
  - 修复了有时退出应用没有保存用户配置的问题；
  - 修复了有时没有正确下载用户头像的问题；
  - 修复了有时退出应用没有向服务器发送 `chat/logout` 事件；
  - 增加了新的个人设置当主窗口失去焦点时自动最小化窗口；
  - 客户端运行文件名更改为英文名称；
  - 优化了喧喧界面及应用图标，现在看起来更正；
  - 开发支持：
    + 修复了在 Windows 平台上的 VSCode 执行调试任务失败的问题；
* **然之服务器端**：
  - 抛弃了基于 PHP 的 socket 实现，所有 API 全部使用 http 实现，配合 xxd 服务器与客户端通信；
* **xxd 服务器**：
  - 新的 xxd 服务与客户端通过 WebSocket 和 https 进行通信，通过 https 或 http 与然之服务器端通信。

### 下载地址：

* Windows 7+：[64 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-win64-setup.exe)、[64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-win64-zip.exe)、[32 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-win32-setup.exe)、[32 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-win32-zip.exe)、[64 位 Debug 安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-debug-win64-setup.exe)
* MacOS：[xuanxuan-1.1.0-mac.dmg](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-mac.dmg)
* Linux：[64 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-linux-x64.tar.gz)、[64 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-linux-amd64.deb)、[64 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-linux-x64.rpm)、[32 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-linux-ia32.tar.gz)、[32 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-linux-i386.deb)、[32 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-linux-ia32.rpm)
* Server: [windows 64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.0-win64.zip)、[windows 32 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.0-win32.zip)、[mac 压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.0-mac.tar.gz)、[linux 64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.0-linux-x64.tar.gz)、[linux 32 位 压缩包](http://dl.cnezsoft.com/xuanxuan/1.1/xxd-1.1.0-linux-ia32.tar.gz)；
* 然之：[xuanxuan-1.1.0-server-rangerteam.zip](http://dl.cnezsoft.com/xuanxuan/1.1/xuanxuan-1.1.0-server-rangerteam.zip)。

## v 1.0.2

[2017-03-13]

修复了一些重要问题：

* 修复了使用 Enter 键发送消息仍然会在消息中插入回车符的问题；
* 修复长时间不使用会掉线的问题；
* 修复用户能够直接发送 HTML 的问题，现在用户在消息中的 HTML 字符都会被转码；
* 修复联系人页面搜索某一用户发送消息后，搜索框仍然显示的问题；
* 修复极端情况下登录成功但返回了其他用户的登录个人信息的问题（当两个用户在同一时间登录可能会发生）；
* 修复使用子目录访问然之导致用户头像无法显示的问题；
* 修复了在 Windows 上最小化后收到消息时没有播放提示音且通知栏图标没有闪烁的问题；
* 现在当窗口处于打开状态但没有激活时收到新消息会闪烁任务栏更易于发现；
* 修复可能会保存未登录成功的用户配置的问题；
* 修复新建一对一会话后会在消息输入框提示重命名的问题（一对一会话无法进行重命名）。

下载地址：

* Windows 7+：[64 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-win64-setup.exe)、[64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-win64-zip.exe)、[32 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-win32-setup.exe)、[32 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-win32-zip.exe)、[64 位 Debug 安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-debug-win64-setup.exe)
* MacOS：[xuanxuan-1.0.2-mac.dmg](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-mac.dmg)
* Linux：[64 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-linux-x64.tar.gz)、[64 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-linux-amd64.deb)、[64 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-linux-x64.rpm)、[32 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-linux-ia32.tar.gz)、[32 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-linux-i386.deb)、[32 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.2-linux-ia32.rpm)

## v 1.0.1

[2017-02-27]

修复了一些问题并增加了 Linux 安装包。

更新明细：

* 增加数据库断线重连的功能，增强服务器端稳定性;
* 增加控制脚本来实现服务器端的启动、停止、重启以及状态查询;
* 修复服务器地址包含端口号时无法找到正确 Socket 服务器 IP 的错误；
* 延长了登录时的等待超时判断时间；
* 禁用 Window 上的系统菜单；
* 开发支持：
  - 客户端开发增加对 DEBUG 版本打包的支持；
  - 增加对 Linux 平台打包的支持；
  - 修复了在 Windows 启动 React 热替换服务的错误；
  - 更新了服务器部署开发文档；

下载地址：

 * Windows 7+：[64 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-win64-setup.exe)、[64 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-win64-zip.exe)、[32 位安装包（.exe）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-win32-setup.exe)、[32 位压缩包](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-win32-zip.exe)
 * MacOS：[xuanxuan-1.0.1-mac.dmg](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-mac.dmg)
 * Linux：[64 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-linux-x64.tar.gz)、[64 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-linux-amd64.deb)、[64 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-linux-x64.rpm)、[32 位（.tar.gz）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-linux-ia32.tar.gz)、[32 位（.deb）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-linux-i386.deb)、[32 位（.rpm）](http://dl.cnezsoft.com/xuanxuan/1.0/xuanxuan-1.0.1-linux-ia32.rpm)

## v 1.0.0

[2017-02-17]

喧喧是由[然之协同](http://ranzhico.com)推出的即时通信解决方案，包括多平台的桌面客户端软件和配合然之协同使用的服务器端插件。

首发版本提供如下特色功能：

* **开聊**：和服务器上的任何用户开聊，收发表情、图片、截屏、文件样样在行；
* **讨论组**：一个人讨论的不过瘾？随时邀请多人组建个性讨论组；
* **公开频道**：将讨论组公开，任何感兴趣的人都可以加入进来；
* **通知及提醒**：与系统桌面环境集成，即时收到新消息通知；
* **会话管理**：将任意会话（包括讨论组和频道）置顶，精彩内容不容错过，还可以重命名讨论组、为讨论组设置白名单及浏览会话的所有消息历史记录；
* **通讯录**：浏览企业成员信息；
* **轻量级服务器端**：轻松搭配[然之协同](http://ranzhico.com)使用。

更多内容参见官方网站：http://xuan.im
