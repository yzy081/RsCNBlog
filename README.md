这个软件的作者同时也是SSCAP、SocksCap64这两个软件的作者，SocksCap64是通过钩子来达到让指定软件/游戏走代理的，在某些软件/游戏中可能会不可用，甚至部分游戏会有封禁风险（当成外挂之类的），所以作者就根据大家的需求，开发一个更好的 代理转全局软件给大家，那就是SSTAP。

简单的介绍一下安装、配置、使用以及各个选项的意思。

SSTAP简单介绍

SSTap全称SOCKSTap, 是一款利用虚拟网卡技术在网络层实现的代理工具。

SSTap能在网络层拦截所有连接并转发给HTTP、SOCKS4/5、Shadowsocks、ShadowsocksR代理。

而无需对被代理的应用程序做任何修改或设置。

它能同时转发TCP、UDP数据包。它非常适合于游戏玩家使用。

SSTAP官方网站：https://www.sockscap64.com/sstap/

SSTAP动态订阅：https://www.sockscap64.com/newsletters-subscribe/

SSTAP Telegram群组：https://t.me/tarolab（SocksCap64/SStap/SScap相关问题讨论）

SSTAP Telegram频道：https://t.me/taronews（SocksCap64/SStap/SScap相关问题讨论）

在使用这个软件代理转全局之前，请先拥有一个可用的Shadowsocks、ShadowsocksR账号并且如果你要玩游戏，那么最好支持UDP转发，否则部分游戏可能会无法链接。

注意：SSTAP并不需要配合Shadowsocks、ShadowsocksR客户端使用。

下载安装

一开始自然是下载安装啦。

SSTAP官方网站：https://www.sockscap64.com/sstap/

SSTAP Telegram频道：https://t.me/taronews（SocksCap64/SStap/SScap相关问题讨论）

大家从上面的官网或者TG频道中下载 SSTAP的压缩包，如SSTap-beta-setup-x.x.x.x.exe.7z文件，使用压缩软件解压这个压缩包，得到一个名为SSTap-beta-setup-x.x.x.x.exe的文件。

我们以管理员身份运行这个文件，会提示你选择安装语言，默认中文，一路下一步即可（选择安装目录的步骤建议改一改，不推荐安装到C盘），然后就会进入安装进度条步骤，安装过程中会提示如下图所示信息：

因为SSTAP想要拦截网络上的所有流量，就必须建立一个虚拟网卡，以此让所有网络流量都经过虚拟网卡，这样才能实现“真 · 全局代理”。

所以安装时需要权限安装OpenVPN的Tap驱动，请允许。

如果不出意外，很快就会安装完毕，然后会自动运行SSTAP。第一次安装SSTAP会看到警告说明：

请认真阅读说明内容，并点击接受按钮。

配置步骤

下面就是SSTAP的主界面了，很简洁，接下来我们就是添加 Shadowsocks/ShadowsocksR代理了。

点击下图红框所圈中的+ 号按钮，然后可以看到三个选项：

添加SOCKS代理…

添加SS/SSR代理…

通过SS/SSR链接批量添加代理…


根据自己的需求选择添加方式，这里以第三个：添加SS/SSR链接批量代理…为例。

选择添加SS/SSR链接批量代理…选项后，就会看到如下界面（当然都是空的），然后我们可以通过ss://链接 或 ssr://链接的方式添加。


链接的获取方式为：在网站用户中心下方的 连接信息 以及 All-in-One(快速配置指导)这一个界面中如图选择WINDOWS之后点击（2 )中的 “这里（普通端口）”之后ssr://链接就会自动复制到剪切板中，粘贴到上面的窗口里点添加就可以了。


添加SS/SSR账号后，我们就在代理下拉框中选择你要使用的SS/SSR代理，并点击下图红框圈中的闪电按钮，就会自动开始测试该SS/SSR账号TCP和UDP是否可用。


请确保TCP可用再继续下面的步骤。（如果TCP不可用，那么请检查SS/SSR账号是否填写错误，如果确定无误，那就检测SS/SSR账号是否本身可用，在确定不是SS/SSR账号的问题后，请携带截图和具体复现步骤说明，前往TG群联系作者解决。）

至于UDP，则取决于你要代理的软件/游戏是否需要使用UDP，如果不需要那就不说了，如果需要UDP转发，那么你的SS/SSR账号也需要支持UDP转发（ShadowsocksR服务端默认开启UDP转发，只要端口开放了，就能用）。在UDP转发不可用的情况下，如果你清楚你要代理的软件/游戏的UDP数据不需要走代理，那么你可以看下面的设置解释，来设置不转发UDP。

在确定添加的SS/SSR代理TCP、UDP都没毛病后，我们就该看代理模式了。

目前版本，暂时有以下五个代理模式：

全局：顾名思义，整个电脑网络所有流量全部都走代理，在不清楚如何选择的时候，选这个就行。

仅网页浏览器（全局）：仅仅让浏览器走代理，不过浏览器访问的所有网页都会走代理。

仅网页浏览器（跳过中国站点）：仅仅让浏览器走代理，但是浏览器访问海外的网页才会走代理，也就是国内网站直连。

仅代理中国IP：在全局的基础上 仅代理中国IP，也就是只有访问国内IP的网络流量才会走代理，一般都是海外用户想要返回国内用的（如玩国服游戏）。

不代理中国IP：与上面相反，这个是在全局的基础上 代理所有访问海外IP的网络流量，而国内IP的都直连，如果你是专玩外服游戏，那么选这个就行。

（由于作者已经停止更新 所以一般玩外服游戏选不代理中国IP就行了 不用管其他）


好了，前面的内容基本介绍的七七八八了，再介绍剩下的一些选项解释，就完了。

其他功能解释

在SSTAP的右下角可以看到一个齿轮图标按钮，点击后会显示一个菜单（如下图所示）。


其中显示日志…、重置流量统计…、支持…、关于…、退出这些就不需要我解释了吧，我主要解释另外几个。

设置选项解释

首先第一个设置选项。

打开后会看到如下图界面，各选项解释：

不转发UDP：指的是SSTAP会让UDP数据直连，而不是走代理。

预选DNS：这里记录了大量目前互联网上公共免费的DNS，默认即可，不懂请不要改动！

首选DNS：同上，默认即可。

备选DNS：同上，默认即可。

代理DNS服务器：指的是你电脑发出的域名解析DNS请求全部走代理（无视代理模式规则）。

开机自启动：勾选后开机后，会自动启动SSTAP。

运行后自动连接：运行SSTAP后，会自动连接上一次关闭SSTAP时所用的SS/SSR代理。

– 延迟链接：针对上面选项的扩展选项，如设置 10秒，那就是运行SSTAP后。等待10秒再自动连接SS/SSR代理。

连接后自动隐藏窗体：SSTAP连接SS/SSR账号成功后，自动隐藏窗口。


附加路由管理解释

平时你如果想要某些IP走 代理 或者 直连，并不需要纠结于代理模式，而是直接在附加路由管理中 添加相关动作即可。

例如：我玩的外服游戏的服务器IP是 2.2.2.2，而因为未知原因导致某个代理模式下，IP 2.2.2.2 不走代理，但是我想让他走代理加速。那我就可以填写IP：2.2.2.2，动作：代理，并点击添加按钮即可。

注意：此功能在连接SSTAP后是无法操作的。


SSR订阅管理

这个功能应该很多人都清楚吧，如果你有SSR的订阅链接，那么可以在这里添加，而更新频率，默认一天就行了。

作者：Baero
链接：https://www.jianshu.com/p/519e68b74646
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
