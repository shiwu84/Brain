For Linux systems with systemd, usually the installation already includes a sing-box service, you can manage the service using the following command:
对于使用 systemd 的 Linux 系统，通常安装时已经自带了 sing-box 服务，你可以使用下面的命令来管理这个服务。

# 🧩 句子结构拆分

| 英文部分                               | 中文含义                    | 语法说明      |
| ---------------------------------- | ----------------------- | --------- |
| **For Linux systems with systemd** | 对于使用 systemd 的 Linux 系统 | 介词短语作状语   |
| **usually**                        | 通常                      | 副词        |
| **the installation**               | 安装（过程/包）                | 主语        |
| **already includes**               | 已经包含                    | 动词短语（现在时） |
| **a sing-box service**             | 一个 sing-box 服务          | 宾语        |
| **you can manage the service**     | 你可以管理这个服务               | 主句        |
| **using the following command**    | 使用下面的命令                 | 介词短语作方式状语 |

# 📝 词汇详解

| 英文单词             | 中文                   | 例句补充                             |
| ---------------- | -------------------- | -------------------------------- |
| **systemd**      | Linux 系统的初始化系统和服务管理器 | 大多数现代 Linux 发行版都用它               |
| **installation** | 安装；安装程序              | "install" 是动词，"installation" 是名词 |
| **includes**     | 包含；包括                | include 的第三人称单数现在时               |
| **sing-box**     | 一种代理/隧道软件            | 常用于科学上网                          |
| **service**      | 服务                   | 后台运行的程序                          |
| **manage**       | 管理；控制                | 如管理、启动、停止                        |
| **following**    | 下面的；接下来的             | 指代后文的内容                          |
| **command**      | 命令                   | 在终端执行的指令                         |

# 📋 命令表格

| 操作 (Operation) | 命令 (Command)                                |
| -------------- | ------------------------------------------- |
| Enable（启用）     | sudo systemctl enable sing-box              |
| Disable（禁用）    | sudo systemctl disable sing-box             |
| Start（启动）      | sudo systemctl start sing-box               |
| Stop（停止）       | sudo systemctl stop sing-box                |
| Kill（强制终止）     | sudo systemctl kill sing-box                |
| Restart（重启）    | sudo systemctl restart sing-box             |
| Logs（查看日志）     | sudo journalctl -u sing-box --output cat -e |
| New Logs（实时日志） | sudo journalctl -u sing-box --output cat -f |

