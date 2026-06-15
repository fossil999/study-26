# 计算机初步入门学习方案

---

### 第一阶段：环境搭建与底层基石（第1-4课）

[x] **第1课：操作系统核心概念与开发环境准备**
- 目标：理解OS作用，搭建统一的实验环境
- 内容：进程/内存/文件系统基本概念；安装Linux虚拟机（Ubuntu）或WSL2；熟悉终端基础命令（ls, cd, ps, top）
- 实操：在虚拟机中执行10个常用命令，查看进程列表
- 作业：完成[Linux 入门：Shell和命令](https://www.lintcode.com/course/66)
- Git：版本控制基本概念（工作区/暂存区/仓库）；常用命令（init/clone/status/add/commit/log/branch/merge/rebase/push/pull）
- 实操：在本地初始化一个仓库并完成3次提交；创建分支并合并；配置远端并推送到GitHub/Gitee

**第2课：虚拟化原理与实操**
- 目标：理解虚拟机与容器，能独立创建快照
- 内容：硬件虚拟化 vs. 容器化（VMware/VirtualBox vs. Docker）；为什么需要隔离环境；快照与克隆
- 实操：用VMware创建一台Ubuntu虚拟机，保存快照；安装Docker并运行hello-world容器

**第3课：网络基础**
- 目标：掌握OSI/TCP-IP模型、IP地址、子网
- 内容：5层模型作用；IP/子网掩码/网关/DNS；ARP与路由原理
- 实操：用ping/traceroute测试连通性；用ipconfig/ifconfig查看本机配置

**第4课：GIT 版本控制**
- 目标：理解版本控制的基本概念，能独立使用
- 内容：版本控制的基本概念（工作区/暂存区/仓库）；常用命令（init/clone/status/add/commit/log/branch/merge/rebase/push/pull）
- 实操：在本地初始化一个仓库并完成3次提交；创建分支并合并；配置远端并推送到GitHub/Gitee
- 作业：完成[Git 入门](https://www.lintcode.com/course/39)

---

### 第二阶段：C语言——理解计算机本质（第5-8课）

**第5课：C语言起步——内存与指针的前置基础**
- [C 语言入门：基本语法及运算](https://www.lintcode.com/course/111)
- [C 语言基础：控制流程语句](https://www.lintcode.com/course/114)
- 目标：掌握变量、类型、地址概念
- 内容：基本数据类型；变量在内存中的存储；取地址符&；指针的直观理解（内存门牌号）
- 实操：编写程序打印变量的地址；用sizeof查看类型字节数

**第6课：指针与数组——栈内存操作**
- [C 语言基础：数组和字符串](https://www.lintcode.com/course/115)
- 目标：理解指针运算与数组本质
- 内容：指针定义与解引用；指针运算；数组与指针的关系；字符串处理（char*）
- 实操：实现一个字符串拷贝函数；用指针遍历数组

**第7课：动态内存分配与结构体**
- [C 语言进阶：指针](https://www.lintcode.com/course/117)
- [C 语言进阶：结构体](https://www.lintcode.com/course/118)
- 目标：区分堆和栈；组织复合数据
- 内容：malloc/free；堆与栈的区别；内存泄漏；结构体的定义与使用
- 实操：动态创建学生结构体数组，并排序

**第8课：C 语言基础：函数**
- [C 语言基础：函数](https://www.lintcode.com/course/116)
- 目标：综合运用指针、内存、文件IO
- 内容：文件操作（fopen/fread）；命令行参数（argc, argv）；实现类似wc或grep简单版
- 实操：编写一个程序，统计文本文件的行数、单词数

---

### 第三阶段：Python——高效开发与工具（第9-10课）

**第9课：Python起步与胶水特性**
- 目标：快速理解动态类型与内置数据结构
- 内容：对比C的内存管理；列表/字典/元组；缩进规则
- 实操：用列表推导式过滤数据

**第10课：Python网络编程与自动化**
- 目标：用Python简化网络操作
- 内容：socket库实现简易聊天程序；requests库发起HTTP请求；用subprocess执行系统命令
- 实操：写一个端口扫描脚本；用Python发送GET请求并解析JSON


---

### 第四阶段：Go语言——工程化与并发（第11-14课）

**第11课：Go起步——语法与工具链**
- 目标：搭建Go开发环境，理解Go的工程结构与基础语法
- 内容：安装Go；GOMOD与go env；package/main；变量/控制流；函数与多返回值；错误处理（error）
- 实操：创建一个Go模块；实现一个命令行计算器（支持add/sub/mul/div）

**第12课：结构体与接口——组合优于继承**
- 目标：掌握Go的类型系统，能用接口组织可替换实现
- 内容：struct与方法；指针接收者 vs 值接收者；interface与隐式实现；常见标准库接口（io.Reader/io.Writer）
- 实操：实现一个可插拔的“存储层”接口（内存版/文件版），并写一个简单的TODO管理器

**第13课：并发编程——Goroutine与Channel**
- 目标：理解Go并发模型，能写出安全、可控的并发程序
- 内容：goroutine；channel与select；context取消；WaitGroup；竞态条件与go test -race
- 实操：实现一个并发爬取器（带并发度限制与超时）；输出统计结果并进行race检查

**第14课：网络服务与工程化——HTTP与可观测性入门**
- 目标：能用Go写一个可运行的HTTP服务，并具备基本工程化能力
- 内容：net/http路由与中间件；JSON编解码；配置与日志；单元测试与基准测试；常用项目布局（cmd/internal/pkg）
- 实操：实现一个REST API（CRUD）；添加基础测试；使用pprof进行简单性能分析
