# Clash规则文件的总结 

## 1. 订阅转换的方法(推荐) 

### 1.1 基本介绍

这种方法采用前后端分离的模式，将订阅链接中的节点全部提取出来，重新分组并重新书写分流规则。

[前端页面](https://acl4ssr-sub.github.io/)负责将所有订阅链接，配置文件的地址，后端解析器的地址，以及一些特殊需求拼接成一个URL链接。

之后访问该链接时，会自动调用后端链接的解析器，解析器会自动下载订阅链接的文件，之后根据配置文件的地址和特殊需求，重新将节点分组，并生成分流的规则，合并成一个文件供下载使用。

### 1.2 使用步骤

1. 在[前端页面](https://acl4ssr-sub.github.io/)中，按照以下方式填写：

   - 订阅链接：填写购买的Clash订阅链接地址
   - 客户端：根据自己的客户端样式选择对应的选项。如：CFW选择ClashR新参数
   - 远程配置：选择规则文件。这里是核心功能，建议使用自己自定义的规则，以满足自己个性化的功能。
   - 后端地址：建议使用 **\[subconverter作者提供-稳定\]**
   - 排除节点：可以排除一些高倍率的节点
   - 输出文件名：最终下载的文件名称。
   - 更多选项：默认即可，需要的可自行探索。
   - 定制功能：默认即可，需要的可自行探索。

ps: 有一种利用worker修改订阅地址，并在之后恢复订阅地址的[安全防泄露的方法](https://github.com/bulianglin/psub/tree/main)。自用的地址为[https://lff.ffli7350.workers.dev/](https://lff.ffli7350.workers.dev/)。

2. 点击生成订阅链接，在定制订阅复制订阅链接。

3. 在CFW粘贴生成的链接，并下载。

### 1.3 可直接使用的规则模板

- 自用订阅转换的规则模板：[cfw_convert_config.ini](https://raw.githubusercontent.com/lifeifan38324/ClashConfig/main/cfw_convert_config.ini)

- 作者ACL4SSR编写的大量规则模板：[ACL4SSR/Clash/config](https://github.com/ACL4SSR/ACL4SSR/tree/master/Clash/config)

- 当然，这些规则模板可以直接在前端转换页面[ACL4SSR在线订阅转换](https://acl4ssr-sub.github.io/)直接使用

### 1.4 自己书写规则模板

详细的订阅文件书写规则请参考[subconverter大神的使用说明](https://github.com/tindy2013/subconverter/blob/master/README-cn.md#%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6) 


---
## 2. 引用外部规则集和代理集的方法 
[参考Loyalsoldier的规则文档](https://github.com/Loyalsoldier/clash-rules#%E7%AE%80%E4%BB%8B) 

