unbound - **Unbound** DNS validating **resolver** 1.24.2.
unbound - 无束缚的DNS验证解析器 1.24.2。

# **SYNOPSIS** 概要

```bash
unbound [-hdpv] [-c <cfgfile>]
```

unbound is a caching DNS resolver.
unbound是一个缓存DNS解析器。

It  uses **a built in list** of **authoritative** nameservers for the root zone (.), **the so called** root hints.
它使用一个内置的权威域名服务器列表，用于根区域（.），即所谓的根提示。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **It** | 代词 | 它 | 指代 Unbound 软件 |
| **uses** | 动词 | 使用 | 利用、采用 |
| **a built in list** | 名词短语 | 内置列表 | 预先装好的列表 |
| **built in** | 形容词 | 内置的、嵌入的 | 预先做好的、附带的 |
| **list** | 名词 | 列表 | 一串名字的清单 |
| **of** | 介词 | ...的 | 表示所属关系 |
| **authoritative** | 形容词 | 权威的 | 正式的、可信的 |
| **nameservers** | 名词 | 域名服务器 | 回答 DNS 问题的服务器 |
| **for** | 介词 | 为了 | 表示用途 |
| **the root zone** | 名词短语 | 根区域 | 互联网的最高级 |
| **(.)** | 符号 | 点 | 代表根区域 |
| **the so called** | 短语 | 所谓的 | 人们这样叫的 |
| **root hints** | 名词短语 | 根提示 | 根服务器的提示信息 |

**On receiving** a DNS query it will ask the root name‐a top level domain (TLD) authoritative nameserver.
当收到一个 DNS 查询时，它会询问根域名服务器——一个顶级域（TLD）权威服务器。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **On receiving** | 介词短语 | 当收到...时 | 表示时间 |
| **receiving** | 动词 | 收到、接收 | 收到（东西） |
| **a DNS query** | 名词短语 | 一个 DNS 查询 | 有人问 DNS 问题 |
| **query** | 名词/动词 | 查询、问题 | 询问、请求 |
| **it will ask** | 动词短语 | 它会询问 | 它会问... |
| **the root** | 名词短语 | 根（服务器） | 最上面的服务器 |
| **name‐server** | 名词 | 域名服务器 | 回答域名问题的服务器 |
| **a top level domain** | 名词短语 | 一个顶级域 | 如 .com .org 等 |
| **top level** | 形容词 | 顶级的、最高级的 | 最高的等级 |
| **domain** | 名词 | 域、域名 | 网站的地址部分 |
| **authoritative** | 形容词 | 权威的 | 正式的、可信的 |
| **nameserver** | 名词 | 域名服务器 | 回答 DNS 问题的服务器 

It will then ask that name‐server for an answer.
然后它会向那个域名服务器请求答案。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **It will then** | 动词短语 | 然后它会 | 表示接下来发生的动作 |
| **then** | 副词 | 然后、接着 | 表示顺序 |
| **ask** | 动词 | 问、询问 | 提出请求 |
| **that** | 代词 | 那个 | 指代前面的服务器 |
| **name‐server** | 名词 | 域名服务器 | 回答 DNS 问题的服务器 |
| **for an answer** | 介词短语 | 要一个答案 | 寻求回复 |

It will recursively continue until an answer is found or no answer is available (NXDOMAIN). 
它会递归地继续下去，直到找到答案或没有答案可用（NXDOMAIN）。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **It will** | 动词短语 | 它会 | 表示将来的动作 |
| **recursively** | 副词 | 递归地 | 一次次重复 |
| **recursively continue** | 动词短语 | 递归继续 | 一次次地问下去 |
| **continue** | 动词 | 继续 | 不停止、接着做 |
| **until** | 连词 | 直到 | 表示结束时间 |
| **an answer** | 名词短语 | 一个答案 | 找到结果 |
| **is found** | 动词短语 | 被找到 | 发现、找到 |
| **or** | 连词 | 或者 | 表示选择 |
| **no answer** | 名词短语 | 没有答案 | 找不到 |
| **is available** | 动词短语 | 是可用的 | 可以得到 |
| **(NXDOMAIN)** | 名词 | 不存在的域名 | "这个域名不存在" |

For performance and efficiency reasons that answer is cached for a certain time (the answer's time-to-live or TTL).
由于性能和效率的原因，那个答案会被缓存一段时间（答案的生存时间，即 TTL）。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **For ... reasons** | 介词短语 | 由于...原因 | 表示理由 |
| **performance** | 名词 | 性能 | 做事快不快 |
| **and efficiency** | 名词短语 | 和效率 | 效率高不高 |
| **reasons** | 名词 | 原因 | 理由 |
| **that answer** | 名词短语 | 那个答案 | 前面找到的 IP |
| **is cached** | 动词短语 | 被缓存 | 被保存起来 |
| **cached** | 动词 | 缓存 | 临时保存 |
| **for a certain time** | 介词短语 | 一段时间 | 一段固定时间 |
| **certain** | 形容词 | 某个、一定的 | 特定的 |
| **the answer's** | 名词短语 | 答案的 | 表示所属 |
| **time-to-live** | 名词短语 | 生存时间 | 能活多久 |
| **or TTL** | 缩写 | 或者 TTL | 全称 |

A second query for the same name will then be answered from the cache.
对同一个名称的第二次查询将直接从缓存中应答。

# 逐词解释

| 英语                        | 词性   | 中文      | 简单解释      |
| ------------------------- | ---- | ------- | --------- |
| **A second query**        | 名词短语 | 第二次查询   | 第二次问同样的问题 |
| **second**                | 序数词  | 第二个     | 第二次       |
| **for the same name**     | 介词短语 | 对于同一个名字 | 同一个网站     |
| **same**                  | 形容词  | 相同的     | 一样的       |
| **name**                  | 名词   | 名字      | 这里指域名     |
| **will then be answered** | 动词短语 | 将被回答    | 会被回复      |
| **answered**              | 动词   | 回答、应答   | 回复        |
| **from the cache**        | 介词短语 | 从缓存     | 从保存的地方    |

Un‐bound can also do DNSSEC validation.
Unbound 还可以进行 DNSSEC 验证。

# 逐词解释

| 英语             | 词性   | 中文      | 简单解释     |
| -------------- | ---- | ------- | -------- |
| **Unbound**    | 名词   | Unbound | 软件名      |
| **can also**   | 动词短语 | 还可以     | 表示额外能力   |
| **also**       | 副词   | 也       | 除此之外还有   |
| **do**         | 动词   | 做、执行    | 进行       |
| **DNSSEC**     | 名词   | DNSSEC  | DNS 安全扩展 |
| **validation** | 名词   | 验证、校验   | 检查是否可信   |

To use a locally running Unbound for resolving put:
要使用本地运行的 Unbound 进行解析，请将：

# 逐词解释

| 英语                    | 词性       | 中文      | 简单解释       |
| --------------------- | -------- | ------- | ---------- |
| **To use**            | 动词不定式    | 要使用     | 表示目的       |
| **use**               | 动词       | 使用、用    | 采用、利用      |
| **a locally running** | 动词短语/形容词 | 本地运行的   | 在自己电脑上跑的   |
| **locally**           | 副词       | 本地地     | 在本地        |
| **running**           | 动词       | 运行、运行中  | 正在运作       |
| **Unbound**           | 名词       | Unbound | 软件名        |
| **for resolving**     | 介词短语     | 用于解析    | 用来做 DNS 查询 |
| **resolving**         | 动词       | 解析      | 查询域名对应的 IP |
| **put:**              | 动词       | 放入、写入   | 放置、填写      |

nameserver 127.0.0.1
**nameserver 127.0.0.1**

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **nameserver** | 名词 | 域名服务器 | DNS 服务器地址 |
| **127.0.0.1** | 名词 | 本地回环地址 | "自己"的 IP 地址 |

into resolv.conf(5).
写入 resolv.conf(5)。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **into** | 介词 | 到...里面 | 表示放入 |
| **resolv.conf** | 名词 | resolv.conf | 配置文件的名字 |
| **(5)** | 数字 | 第5节 | 手册页的章节号 |

If authoritative DNS is needed as well using nsd(8), careful setup is required because authoritative nameservers and resolvers are using the same port number (53).
如果还需要使用 nsd(8) 提供权威 DNS 服务，则需要仔细配置，因为权威域名服务器和解析器使用相同的端口号（53）。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **If** | 连词 | 如果 | 条件 |
| **authoritative DNS** | 名词短语 | 权威 DNS | 权威域名服务 |
| **is needed** | 动词短语 | 被需要 | 需要 |
| **as well** | 副词短语 | 也、还 | 除了这个还有 |
| **using nsd(8)** | 动词短语 | 使用 nsd(8) | 用 nsd 软件 |
| **careful setup** | 名词短语 | 仔细的配置 | 小心设置 |
| **is required** | 动词短语 | 是必须的 | 需要 |
| **because** | 连词 | 因为 | 解释原因 |
| **authoritative nameservers** | 名词短语 | 权威域名服务器 | 提供域名答案的服务器 |
| **and** | 连词 | 和 | 连接 |
| **resolvers** | 名词 | 解析器 | 查询域名的程序 |
| **are using** | 动词短语 | 正在使用 | 使用中 |
| **the same** | 形容词短语 | 相同的 | 一样的 |
| **port number** | 名词短语 | 端口号 | 网络端口 |
| **(53)** | 数字 | 53 | DNS 默认端口 |

The available options are:
可用的选项如下：

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **The available** | 形容词短语 | 可用的 | 能用的、存在的 |
| **available** | 形容词 | 可用的 | 可以使用的 |
| **options** | 名词 | 选项、参数 | 命令后面的参数 |

-h     Show the version number and commandline option help, and exit.
-h     显示版本号和命令行选项帮助，然后退出。

# 逐词解释

| 英语                     | 词性   | 中文       | 简单解释    |
| ---------------------- | ---- | -------- | ------- |
| **-h**                 | 标志   | -h（帮助参数） | 查看帮助信息  |
| **Show**               | 动词   | 显示、展示    | 打开给你看   |
| **the version number** | 名词短语 | 版本号      | 软件的版本   |
| **commandline**        | 名词   | 命令行      | 终端里写的命令 |
| **commandline option** | 名词短语 | 命令行选项    | 命令后面的参数 |
| **help**               | 名词   | 帮助       | 使用说明    |
| **and exit**           | 动词短语 | 然后退出     | 退出程序    |

-c <cfgfile>  Set the config file with settings for unbound to read instead of reading the file at the default location, /etc/unbound/unbound.conf.  The syntax is described in unbound.conf(5).

-c <配置文件> 指定 Unbound 读取的配置文件，而不是读取默认位置的 /etc/unbound/unbound.conf。语法在 unbound.conf(5) 中有描述。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **-c** | 标志 | -c（配置参数） | 指定配置文件 |
| **<cfgfile>** | 名词 | 配置文件 | config file 的缩写 |
| **Set** | 动词 | 设置、指定 | 设定 |
| **the config file** | 名词短语 | 配置文件 | 设置文件 |
| **with settings** | 介词短语 | 带着设置 | 包含配置 |
| **for unbound** | 介词短语 | 给 Unbound | Unbound 用的 |
| **to read** | 动词不定式 | 读取 | 加载 |
| **instead of** | 介词短语 | 而不是 | 代替 |
| **reading** | 动词 | 读取 | 加载 |
| **the file at the default location** | 名词短语 | 默认位置的文件 | 原来位置的文件 |
| **default** | 形容词 | 默认的 | 标准的、预设的 |
| **location** | 名词 | 位置 | 地点 |
| **/etc/unbound/unbound.conf** | 路径 | 配置文件默认位置 | Linux 系统配置文件 |
| **The syntax** | 名词短语 | 语法 | 格式、规则 |
| **is described** | 动词短语 | 被描述 | 有说明 |
| **in unbound.conf(5)** | 介词短语 | 在 unbound.conf(5) 中 | 手册的第5章 |

 -d     Debug  flag:do  not  fork  into  the  background,but  stay attached to the console.  This flag will also delay writing to the log file until the thread-spawn time, so that most config and setup errors appear on stderr.  If given twice or more, logging does not switch to the  log  file  or  to syslog, but the log messages are printed to stderr all the time.
-d     调试标志：不后台运行，而是保持在终端窗口。这个标志还会延迟写入日志文件，直到线程创建时间，以便大多数配置和设置错误显示在 stderr 中。如果使用两次或更多，日志不会切换到日志文件或 syslog，但日志消息会始终打印到 stderr。
# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **-d** | 标志 | -d（调试参数） | 调试模式 |
| **Debug flag** | 名词短语 | 调试标志 | 开启调试功能 |
| **do not fork** | 动词短语 | 不分叉 | 不后台运行 |
| **fork** | 动词 | 分叉 | 程序"生出一个副本"去后台运行 |
| **into the background** | 介词短语 | 到后台 | 在后台运行 |
| **but** | 连词 | 而是 | 对比 |
| **stay** | 动词 | 保持、停留 | 留在 |
| **attached to** | 动词短语 | 附着在 | 连接到 |
| **the console** | 名词短语 | 控制台 | 终端屏幕 |
| **This flag** | 名词短语 | 这个标志 | -d 参数 |
| **will also** | 动词短语 | 也会 | 额外的作用 |
| **delay** | 动词 | 延迟 | 推迟 |
| **writing to the log file** | 动词短语 | 写入日志文件 | 记录日志 |
| **until** | 介词 | 直到 | 等到 |
| **the thread-spawn time** | 名词短语 | 线程创建时间 | 程序开始运行时 |
| **so that** | 连词 | 以便 | 目的 |
| **most config and setup errors** | 名词短语 | 大多数配置和设置错误 | 启动时的错误 |
| **appear** | 动词 | 出现 | 显示 |
| **on stderr** | 介词短语 | 在标准错误输出 | 屏幕上（不是日志） |
| **If given twice or more** | 条件句 | 如果用两次或更多 | -d -d 或 -dd |
| **logging does not switch** | 动词短语 | 日志不会切换 | 不改变日志位置 |
| **to the log file** | 介词短语 | 到日志文件 | 不写文件 |
| **or to syslog** | 介词短语 | 或 syslog | 也不写系统日志 |
| **but the log messages are printed** | 动词短语 | 但是日志消息被打印 | 但是会显示 |
| **to stderr all the time** | 介词短语 | 一直写到 stderr | 一直显示在屏幕上 |

-p     Don't  use  a pidfile.  This argument should only be used by supervision systems which can ensure that only one instance of Unbound will run concurrently.
-p     不使用 pidfile。这个参数只应该由监督系统使用，以确保只有一个 Unbound 实例同时运行。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **-p** | 标志 | -p（不使用 pidfile） | 不创建进程文件 |
| **Don't use** | 动词短语 | 不使用 | 不要用 |
| **a pidfile** | 名词短语 | pid 文件 | 进程ID文件 |
| **pidfile** | 名词 | 进程标识文件 | 记录进程号的文件 |
| **This argument** | 名词短语 | 这个参数 | -p |
| **should only be used** | 动词短语 | 只应该被使用 | 最好只用 |
| **by supervision systems** | 介词短语 | 由监督系统 | 由监控软件 |
| **which can ensure** | 定语从句 | 可以确保 | 能够保证 |
| **that only one instance** | 名词短语 | 只有一个实例 | 只有一个程序在跑 |
| **of Unbound** | 介词短语 | Unbound 的 | Unbound 程序 |
| **will run** | 动词短语 | 会运行 | 正在运行 |
| **concurrently** | 副词 | 同时地 | 并发地 |

-v     Increase verbosity.  If given multiple times, more information is logged.  This is in addition to the verbosity (if any) from the config file.
-v     增加详细程度。如果多次使用，会记录更多信息。这是在配置文件中的详细程度（如果有的话）之外的。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **-v** | 标志 | -v（详细模式） | 增加日志详细度 |
| **Increase** | 动词 | 增加、提高 | 调高 |
| **verbosity** | 名词 | 详细程度、冗余度 | 日志信息多少 |
| **If given multiple times** | 条件句 | 如果多次给出 | -v -v 或 -vv |
| **more information** | 名词短语 | 更多信息 | 更详细的日志 |
| **is logged** | 动词短语 | 被记录 | 会被写入日志 |
| **This is in addition to** | 动词短语 | 这是在...之外 | 还要加上 |
| **the verbosity** | 名词短语 | 详细程度 | 日志级别 |
| **if any** | 条件句 | 如果有的话 | 配置文件里可能有 |
| **from the config file** | 介词短语 | 从配置文件 | 来自设置文件 |

-V     Show the version number and build options, and exit.
-V     显示版本号和编译选项，然后退出。

# 逐词解释

| 英语 | 词性 | 中文 | 简单解释 |
|------|------|------|----------|
| **-V** | 标志 | -V（大写，版本参数） | 查看完整版本信息 |
| **Show** | 动词 | 显示 | 展示 |
| **the version number** | 名词短语 | 版本号 | 软件版本 |
| **and build options** | 名词短语 | 和编译选项 | 怎么编译的 |
| **build options** | 名词短语 | 编译选项 | 编译时的设置 |
| **and exit** | 动词短语 | 然后退出 | 退出程序 |
