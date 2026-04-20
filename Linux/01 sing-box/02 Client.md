# Introduction

For a long time, the modern usage and principles of proxy clients for graphical operating systems have not been clearly described. 
长期以来，图形操作系统代理客户端的现代使用方式和原理一直没有被清晰地描述。

**句子成分拆分：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 时间状语 | For a long time | 长期以来 |
| 主语 | the modern usage and principles of proxy clients for graphical operating systems | 图形操作系统代理客户端的现代使用方式和原理 |
| 谓语 | have not been clearly described | 一直没有被清晰地描述（现在完成时的被动语态，否定形式） |

**词汇解释：**

- **For a long time** = 长期以来（表示持续的时间）
- **modern usage** = 现代用法/现代使用方式
- **principles** = 原理（复数形式）
- **proxy clients** = 代理客户端（软件）
- **graphical operating systems** = 图形操作系统（如 Windows、macOS、Linux 桌面版）
- **have not been described** = 从未被描述（现在完成时被动语态的否定形式）

**语法点：**

- 现在完成时（have + 过去分词）表示从过去持续到现在的状态
- 被动语态（be + 过去分词）表示主语承受动作

However, we can categorize them into three types: system proxy, firewall redirection, and virtual interface.
然而，我们可以将它们（代理客户端）分为三种类型：系统代理、防火墙重定向和虚拟接口。

**句子成分拆分：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 连接副词 | However | 然而（表示转折） |
| 主语 | we | 我们 |
| 谓语 | can categorize | 可以分类 |
| 宾语 | them into three types | 将它们分为三种类型 |
| 同位语（冒号后）| system proxy, firewall redirection, and virtual interface | 系统代理、防火墙重定向和虚拟接口 |

**词汇解释：**

- **However** = 然而（表示转折对比，与上一句的"没有清晰描述"形成对比）
- **categorize** = 分类，归纳
- **them** = 它们（指代前一句的 proxy clients）
- **into three types** = 分成三种类型
- **system proxy** = 系统代理（操作系统级别的代理设置）
- **firewall redirection** = 防火墙重定向（通过防火墙规则将流量重定向到代理）
- **virtual interface** = 虚拟接口（创建虚拟网卡来分流代理流量）

# System Proxy

Almost all graphical environments support system-level proxies, which are essentially ordinary HTTP proxies that only support TCP.
几乎所有图形环境都支持系统级代理，这些代理本质上就是普通的 HTTP 代理，只支持 TCP 协议。

# 句子成分拆分

**第一部分（主句）：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 主语 | Almost all graphical environments | 几乎所有图形环境 |
| 谓语 | support | 支持 |
| 宾语 | system-level proxies | 系统级代理 |

**第二部分（非限制性定语从句）：**

| 成分                    | 英文                    | 中文含义                       |
| --------------------- | --------------------- | -------------------------- |
| 关系代词                  | which                 | 替代前面的 system-level proxies |
| 系动词                   | are                   | 是                          |
| 状语                    | essentially           | 本质上                        |
| 表语                    | ordinary HTTP proxies | 普通的 HTTP 代理                |
| 定语从句（修饰 HTTP proxies） | that only support TCP | 只支持 TCP 的                  |

# 词汇解释

| 英文                         | 中文      | 说明                                              |
| -------------------------- | ------- | ----------------------------------------------- |
| **Almost all**             | 几乎所有    | 表示数量接近全部                                        |
| **graphical environments** | 图形环境    | 指有 GUI（图形用户界面）的操作系统环境，如 Windows、macOS、Linux 桌面版 |
| **system-level**           | 系统级的    | 在操作系统层面生效的，不是单个应用程序级别的                          |
| **proxies**                | 代理      | 复数形式，指代理服务/软件                                   |
| **essentially**            | 本质上     | 相当于 "basically" 或 "in nature"                   |
| **ordinary**               | 普通的     | 强调是标准、最常见的类型                                    |
| **HTTP proxies**           | HTTP 代理 | 基于 HTTP 协议的代理                                   |
| **TCP**                    | 传输控制协议  | 一种面向连接的传输层协议，代理最常用的协议                           |

As one of the most well-known proxy methods, it has many shortcomings: many TCP clients that are not based on HTTP do not check and use the system proxy. Moreover, UDP and ICMP traffics bypass the proxy.
作为最著名的代理方法之一，它（系统代理）有很多缺点：许多不是基于 HTTP 的 TCP 客户端不会检查和使用系统代理。

**句子成分拆分：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 状语（介词短语）| As one of the most well-known proxy methods | 作为最著名的代理方法之一 |
| 主语 | it | 它（指代前文提到的 system proxy） |
| 谓语 | has | 有 |
| 宾语 | many shortcomings | 很多缺点 |
| 同位语（冒号后）| many TCP clients that are not based on HTTP do not check and use the system proxy | 许多不是基于 HTTP 的 TCP 客户端不会检查和使用系统代理 |

**词汇解释：**

- **As** = 作为
- **one of the most well-known** = 最著名的之一（well-known 是知名，most well-known 是最高级）
- **shortcomings** = 缺点，短处
- **TCP clients** = TCP 客户端（使用 TCP 协议的软件/应用）
- **are not based on HTTP** = 不是基于 HTTP 的
- **do not check and use** = 不会检查和使用

# Firewall Redirection防火墙重定向

This type of usage typically relies on the firewall or hook interface provided by the operating system, such as Windows’ WFP, Linux’s redirect, TProxy and eBPF, and macOS’s pf.
这种使用方式通常依赖于操作系统提供的防火墙或钩子接口，例如 Windows 的 WFP、Linux 的 redirect、TProxy 和 eBPF，以及 macOS 的 pf。

**句子成分拆分：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 主语 | This type of usage | 这种使用方式 |
| 谓语 | typically relies on | 通常依赖于 |
| 宾语 | the firewall or hook interface | 防火墙或钩子接口 |
| 定语（provided by 短语）| provided by the operating system | 由操作系统提供的 |
| 状语（such as 短语）| such as Windows' WFP, Linux's redirect, TProxy and eBPF, and macOS's pf | 例如 Windows 的 WFP、Linux 的 redirect、TProxy 和 eBPF，以及 macOS 的 pf |

**词汇解释：**

| 英文                 | 中文                              | 说明                             |
| ------------------ | ------------------------------- | ------------------------------ |
| **relies on**      | 依赖于                             | rely on = 依赖                   |
| **firewall**       | 防火墙                             | 网络安全组件                         |
| **hook interface** | 钩子接口                            | 操作系统提供的编程接口，可以拦截/修改网络流量        |
| **WFP**            | Windows Filtering Platform      | Windows 过滤平台，Windows 系统的网络过滤框架 |
| **redirect**       | 重定向                             | Linux 中用于流量重定向的机制              |
| **TProxy**         | Transparent Proxy               | Linux 的透明代理模块                  |
| **eBPF**           | extended Berkeley Packet Filter | Linux 内核的扩展伯克利数据包过滤器，可动态运行代码   |
| **pf**             | packet filter                   | macOS/BSD 的防火墙工具               |

Although it is intrusive and cumbersome to configure, it remains popular within the community of amateur proxy open source projects like V2Ray, due to the low technical requirements it imposes on the software.
虽然它（防火墙重定向）具有侵入性且配置繁琐，但它在 V2Ray 等业余代理开源项目社区中仍然很流行，因为该方式对软件的技术要求较低。

**句子成分拆分：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 状语（although 从句）| Although it is intrusive and cumbersome to configure | 虽然它具有侵入性且配置繁琐 |
| 主语 | it | 它（指代防火墙重定向方式） |
| 谓语 | remains popular | 仍然流行 |
| 状语（in 短语）| within the community of amateur proxy open source projects | 在业余代理开源项目社区中 |
| 定语（like 短语）| like V2Ray | 例如 V2Ray |
| 原因状语（due to 短语）| due to the low technical requirements it imposes on the software | 由于它对软件的技术要求较低 |

**词汇解释：**

| 英文                       | 中文       | 说明                 |
| ------------------------ | -------- | ------------------ |
| **Although**             | 虽然，尽管    | 从属连词，引导让步状语从句      |
| **intrusive**            | 侵入性的     | 需要修改系统底层设置         |
| **cumbersome**           | 繁琐的，麻烦的  | 难以配置和管理的           |
| **remains**              | 仍然是，保持   | remain = 保持（状态）    |
| **popular**              | 流行的，受欢迎的 |                    |
| **community**            | 社区       | 指开发者/用户群体          |
| **amateur**              | 业余的      | 非专业开发的             |
| **open source projects** | 开源项目     |                    |
| **due to**               | 由于，因为    | 表示原因               |
| **imposes on**           | 施加于      | impose on = 把……强加于 |

# Virtual Interface虚拟接口

All L2/L3 proxies (seriously defined VPNs, such as OpenVPN, WireGuard) are based on virtual network interfaces, which is also the only way for all L4 proxies to work as VPNs on mobile platforms like Android, iOS.
所有 L2/L3 代理（严格定义的 VPN，如 OpenVPN、WireGuard）都基于虚拟网络接口，这也是所有 L4 代理在 Android、iOS 等移动平台上作为 VPN 运行的唯一方式。

**句子成分拆分：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 主语 | All L2/L3 proxies | 所有 L2/L3 代理 |
| 同位语（括号内容）| seriously defined VPNs, such as OpenVPN, WireGuard | 严格定义的 VPN，如 OpenVPN、WireGuard |
| 谓语 | are based on | 基于 |
| 宾语 | virtual network interfaces | 虚拟网络接口 |
| 非限制性定语从句 | which is also the only way for all L4 proxies to work as VPNs on mobile platforms like Android, iOS | 这也是所有 L4 代理在移动平台上作为 VPN 运行的唯一方式 |

**词汇解释：**

| 英文                             | 中文        | 说明                         |
| ------------------------------ | --------- | -------------------------- |
| **L2/L3 proxies**              | 第二层/第三层代理 | OSI 模型的第二层（数据链路层）和第三层（网络层） |
| **seriously defined VPNs**     | 严格定义的 VPN | 真正符合 VPN 定义的隧道技术           |
| **OpenVPN**                    | OpenVPN   | 一种开源 VPN 协议                |
| **WireGuard**                  | WireGuard | 一种现代的开源 VPN 协议             |
| **virtual network interfaces** | 虚拟网络接口    | 操作系统创建的虚拟网卡                |
| **the only way**               | 唯一的方式     |                            |
| **L4 proxies**                 | 第四层代理     | 传输层代理（如 SOCKS、HTTP 代理）     |
| **mobile platforms**           | 移动平台      | Android、iOS 等手机系统          |

The sing-box inherits and develops clash-premium’s TUN inbound (L3 to L4 conversion) as the most reasonable method for performing transparent proxying.
sing-box 继承并发展了 clash-premium 的 TUN 入站（L3 到 L4 转换），将其作为执行透明代理最合理的方法。

**句子成分拆分：**

| 成分 | 英文 | 中文含义 |
|------|------|----------|
| 主语 | The sing-box | sing-box（一个代理软件） |
| 谓语 | inherits and develops | 继承并发展 |
| 宾语 | clash-premium's TUN inbound | clash-premium 的 TUN 入站 |
| 同位语（括号内容）| L3 to L4 conversion | L3 到 L4 的转换 |
| 状语 | as the most reasonable method | 作为最合理的方法 |
| 目的状语 | for performing transparent proxying | 用于执行透明代理 |

**词汇解释：**

| 英文 | 中文 | 说明 |
|------|------|------|
| **inherits** | 继承 | 从已有项目中获取功能 |
| **develops** | 发展，改进 | 在继承基础上进行优化 |
| **clash-premium** | clash-premium | 一个代理订阅转换工具的增强版本 |
| **TUN inbound** | TUN 入站 | TUN 模式是一种虚拟网卡模式 |
| **L3 to L4 conversion** | 第三层到第四层的转换 | 将网络层流量转为传输层流量 |
| **transparent proxying** | 透明代理 | 不需要客户端手动配置的代理方式 |
| **the most reasonable** | 最合理的 | reasonable = 合理的，most reasonable 是最高级 |
