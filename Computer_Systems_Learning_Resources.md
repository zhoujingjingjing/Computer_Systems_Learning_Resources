# 计算机系统学习资源

## 一份推荐清单

## 1 预备知识（Preliminary）

### 免责声明（Disclaimer）

- 本文聚焦**广度（breadth）**而非**深度（depth）**。
- 本文主要关注**软件系统**，较少涉及 VLSI、存储系统和嵌入式系统等主题（尽管在下面部分资源中会提到它们）。

### 阅读方向（Directions）

- 计算机系统最基本的组成部分是：
  1. 计算机体系结构
  2. 操作系统（OS）
  3. 计算机网络
  4. 编译器
  5. 程序设计语言（PL）

  在进入其他部分之前先掌握它们。**第 2–10 节是本清单的核心。**
- 每节中的资源按**适合学习的顺序**排列。
  - 如果时间有限，你可以只读第一本（或前几本）书，然后进入下一节。
  - 要理解一些高级书籍，可能需要后续章节的知识。
- 参考文献帮你定位**作者**，而不是**最新版本**。
- 鉴于计算机科学发展迅速，永远读最新版本。
  - 在 *Amazon* 上搜索最新版本。本文中的版本号可能因新出版物而过时。

### 如何读一本书？

三遍读法：

1. **快速（Fast）**：抓住主旨，忽略所有细节。
2. **穷尽（Exhaustive）**：理解逻辑和几乎所有细节；少数真正难点可跳过。
3. **深入（Deep）**：提出问题，聚焦有趣或困难的点。

这里有一篇著名论文《如何阅读一篇论文》，讨论类似问题：<https://web.stanford.edu/class/cs245/readings/how-to-read-a-paper.pdf>

### 你为什么推荐这么多关于应用的资源？

学会**用**它，然后再学怎么**构建**它。

### 先修知识（Prerequisites）

- **CSAPP**（第 3 版）[16]
- **C/C++**
- **数据结构与算法**
  - 《算法导论》（第 4 版）[19]
- **概率论**
  - 随机过程基础，尤其是一些基本结论和推论，会有帮助。
- **逻辑、自动机与计算复杂性**

### 关于先修知识的特别说明

列出先修知识的目的是帮你画出好的学习路线图。即使你不满足先修条件，也仍可学习该主题；但这样的话，如果你在学习中遇到困难，可以回头参考先修知识，判断是否需要先学别的。

### 如果我想了解更多呢？

1. 搜索顶尖大学开设的更多课程。
   - **如何找到它们？**
     (a) 对某所大学，搜索它的课程列表（注意你要搜的关键词可能不出现在课程名中）。例如：
     - 斯坦福：<https://cs.stanford.edu/academics/courses>
     - UC Berkeley：<https://www2.eecs.berkeley.edu/Courses/CS/>
     - MIT：<http://catalog.mit.edu/subjects/6/>
     (b) 为节省浏览整个课程目录的时间，你可以查找本科/硕士学位的课程表（program sheet）。例如：
     - 斯坦福计算机科学硕士项目课程表：<https://cs.stanford.edu/academics/current-masters/masters-program-sheets/programsheets>
       - i. 低年级（Lower Division）：<https://eecs.berkeley.edu/resources/undergrads/cs/degree-reqs-lowerdiv>
       - ii. 高年级（Upper Division）：<https://eecs.berkeley.edu/resources/undergrads/cs/degree-reqs-upperdiv>
   - 课程编号的命名约定帮你节省时间。
   - 此外，课程提供**实践机会**，这对学习计算机系统很关键。
2. 找到像机器学习系统这样的交叉领域。你总能在这里找到前沿技术和研究热点。此外，当不同模块协同工作时，计算机系统极其强大。
   - 同样，搜索高级课程帮你发现这些领域！

### 如何避免遗忘？

- 重复（多次通读）
- 实践
- 提问
- 讨论

## 2 计算机体系结构（Computer Architecture）

1. 《计算机组成与设计：硬件/软件接口》（第 5 版 [44] / RISC-V 版 [43] / ARM 版 [45]）
   - 原版基于 MIPS。推荐 RISC-V 版；读完此版后可继续读 ARM 版，它是学习 ARM 的好书。
2. 《数字设计与计算机体系结构》（第 2 版 [27] / RISC-V 版 [28] / ARM 版 [26]）
   - 你可以只读第 1–5 章。
   - 原版基于 MIPS。
3. 《RISC-V Reader：开放架构图谱》[42]
4. 《计算机体系结构：量化研究方法》（第 6 版）[29]
   - 第一次读这本书时可以跳过附录。
   - 尽管这本书对新手来说有难度，但它就是"新手的第二本书"。如果你想深入理解某个具体主题，去读 NVIDIA 等厂商的官方教程/文档。
   - 有了并行计算经验后，再回头读这本书的相应章节，你定会获得新的理解。
   - 以我个人经验，要彻底吃透这部杰作，需要多遍阅读。
5. RISC-V 特权体系结构（幻灯片）：<https://riscv.org/wp-content/uploads/2018/05/riscv-privileged-BCN.v7-2.pdf>
   - 关于 RISC-V 特权体系结构、以及"什么是特权体系结构"这一核心问题的精彩幻灯片。
   - 这节课的视频可在 <https://www.youtube.com/watch?v=fxLXvrLN5jA> 找到。
   - 大多数讲计算机体系结构的书很少讨论**特权体系结构**，导致理解 OS 内核时遇到很大困难。请始终记住：ISA 由非特权体系结构和特权体系结构两部分组成。
6. RISC-V 规范：<https://riscv.org/technical/specifications/>
   - 尽管内容详尽，对新手和专家都是极好的书！
   - 附录 A：《RWM0 详解 RISC-V 指令集手册 卷一：非特权 ISA》，是讲**内存一致性**的精彩教程！
7. 《计算机体系结构的新黄金时代》（图灵奖全文演讲）：<https://cacm.acm.org/magazines/2019/2/234352-a-new-golden-age-for-computer-architecture/fulltext>
   - Hennessy 和 Patterson 的著名图灵演讲。大师的深刻洞见！
8. 先修知识：
   - **程序设计语言（PL）**
     - Java。
9. 要实践你的计算机体系结构知识，基本有两条路：
   - VLSI（超大规模集成电路）
   - 并行计算

## 3 操作系统（Operating Systems, OS）

### 3.1 操作系统原理

1. 书籍
   (a) 《操作系统：三个简单部分》：<https://pages.cs.wisc.edu/~remzi/OSTEP/>
     - 由于作者的研究兴趣，这本书非常强调文件系统。第一次读时可以跳过部分章节。
     - 这只是入门级的书，读完后再回头读！
   (b) 《操作系统原理与实践》（第 2 版）
     - 共四卷：
       - 卷 I：内核与进程 [7]
       - 卷 II：并发 [4]
       - 卷 III：内存管理 [5]
       - 卷 IV：持久存储 [6]
   (c) 《操作系统概念》（第 10 版）[46]
     - 非常新，可以作为前一本的替代。两本不必都读。
   (d) xv6 源码与教材：<https://pdos.csail.mit.edu/6.828/2021/xv6.html>
     - 用真实 OS 动手实践不可或缺，xv6 是极好的起点！
   (e) 补充书籍
     i. 《Linux 内核开发》（第 4 版）[51]
     ii. 《深入理解 Linux 内核》（第 3 版）[14]
     iii. 《Linux 设备驱动程序》（第 3 版）[52]
     iv. 《深入理解 Linux 网络内幕》（第 1 版）[12]
2. 课程
   - **实验型（Lab-based）**
     (a) 斯坦福 CS 140E 操作系统设计与实现
       - Rust 版：<https://cs140e.sergio.bz/>
       - C 版：<https://github.com/dddrrreee/cs140e-22win>
       - 独特之处：
         i. "本课程与大多数其他 OS 课程不同，它使用**真实硬件**而非假模拟器，而且几乎所有代码都由你自己写。"
     (b) 斯坦福 CS 240LX 高级系统实验（加速版）：<https://github.com/dddrrreee/cs140e-22win>
       - 独特之处：
         i. "我们的代码将在广泛使用的 ARM 树莓派上'裸金属'运行（不带操作系统）。"
   - **论文型（Paper-based）**
     (a) 斯坦福 CS 240 操作系统高级专题：<http://web.stanford.edu/class/cs240/>
3. 先修知识：
   - 必修：
     (a) 计算机体系结构（尤其是特权体系结构）
   - **程序设计语言（PL）**
     - Java：JVM、GC、Thread、Monitor。
     - Go：Goroutine、Channel、CSP（通信顺序进程）、异步。
4. 建议：
   - 对 OS 读四遍
     (a) 第一遍：从用户/程序员视角，自顶向下。借助 CSAPP 和《Linux 编程》资源。
     (b) 第二遍：从构建者视角，自底向上（构建一个可用的）。
     (c) 第三遍：设计视角（如果没有兼容性问题就构建一个好的）；两个视角都做。这一遍只能靠计算机系统各主要部分的知识才能完成。
     (d) 高级与交叉问题：分布式系统、云计算……
   - 始终思考它们之间的交互与协作：
     - OS 与硬件
     - OS 与计算机网络
     - OS 与程序设计语言
     - OS 与数据库
   - 还要思考它们的边界是否可以、且应该被重新定义。
   - **不要过度模仿 Linux！** 并非其中一切都合理、都适合当前需要。

### 3.2 Linux 编程

1. Linux man 手册页
   - 在 Linux shell 中用 `man` 命令，如 `man fork` 或 `man 2 fork`，其中 "2" 指定卷号。
   - Linux man 手册在线：<https://man7.org/linux/man-pages/>
2. 《UNIX 环境高级编程》（第 3 版）[57]

## 4 计算机网络（Computer Networks）

1. 书籍
   (a) 《计算机网络：自顶向下方法》（第 8 版）[32]
   (b) 补充（作者 W. Richard Stevens）
     - 《UNIX 网络编程》
       - 卷 1，第 3 版：套接字网络 API [56]
       - 卷 2，第 2 版：进程间通信 [49]
     - 《TCP/IP 详解》
       - 卷 1：协议（第 2 版）[21]
       - 卷 2：实现 [58]
       - 卷 3：事务、HTTP、NNTP 和 UNIX 域协议 [59]
2. 课程
   (a) 斯坦福 CS 144 计算机网络导论：<https://cs144.github.io/>
   (b) 斯坦福 CS 244 网络高级专题：<https://2022-cs244.github.io/schedule/>
   (c) 斯坦福 CS 249I 现代互联网：<https://cs249i.stanford.edu/>
   (d) 斯坦福 CS 344 计算机网络专题（又名"构建一个互联网路由器"）：<https://cs344.stanford.io/>
3. 先修知识：
   - 必修：
     (a) 操作系统
   - **程序设计语言（PL）**
     - Java。
     - Python：与 POSIX 类似但更简单的 socket 接口。
     - Go：RPC。

## 5 编译器（Compilers）

编译器在计算机系统中的地位：

1. **编译器**和**程序设计语言**共同构成软件的基础。
2. 多个领域的技术在编译器中被重度运用：
   (a) 计算机体系结构
   (b) 程序设计语言
   (c) 理论计算机科学（自动机、算法、数据结构）
   (d) 离散数学
   (e) 代数
3. 编译器在软硬件协同设计中扮演重要角色，因为它是硬件与程序设计语言之间的桥梁。
4. 不要把编译器仅仅看作从程序设计语言到汇编的翻译工具。广义上，任何自动技术都可视为编译器技术的一部分（而自动化正是基于形式化）。

1. 书籍
   (a) 《编译原理：技术与工具》（第 2 版）[3]
     - "龙书"。
     - 著名但有点过时；对新手仍极好。
   (b) 《现代编译原理：C 语言描述》[9] / Java 版（第 2 版）[10] / ML [8]
     - "虎书"。
   (c) 《高级编译器设计实现》[39]
     - "鲸书"。
   (d) 《编译工程》（第 2 版）[18]
   (e) 《编译精要：增量方法》：<https://jeapostrophe.github.io/courses/2018/spring/406/notes/book.pdf>
   (f) 《实现函数式语言：教程》：<https://www.microsoft.com/en-us/research/wp-content/uploads/1992/01/student.pdf>
2. 课程
   (a) 斯坦福 CS 143 编译原理：<https://web.stanford.edu/class/cs143/>
   (b) 斯坦福 CS 243 程序分析与优化：<https://suif.stanford.edu/courses/cs243/>
   (c) 斯坦福 CS 343D 领域特定编程语言与编译器：<https://cs343d.github.io/>
3. 程序设计建议：
   (a) 试试函数式语言！
     - 模式匹配、组合子、单子设计、强大的类型系统（尤其是代数数据类型）都是你的好朋友！
   (b) 有两种（领域特定）语言：内部的和外部的；后者指一门语言嵌入另一门宿主语言。为一门内部（领域特定）语言写编译器会很有乐趣。好的语言选择：Scala、Haskell、C++。
4. 解析生成器（Parser Generators）
   (a) C/C++：Lex & Yacc [34]
   (b) OCaml：OCamllex & Menhir
     - <https://dev.realworldocaml.org/parsing-with-ocamllex-and-menhir.html>
   (c) Haskell：解析组合子（Parsec）
     - Haskell 中有多种。一些教程：
       i. 《Real World Haskell》：<https://book.realworldhaskell.org/read/using-parsec.html>
       ii. Wikibook：<https://en.wikibooks.org/wiki/Parsing_a_simple_imperative_language>
   (d) F#：FsLex & FsYacc
     - Wikibook 教程：<https://en.wikibooks.org/wiki/F_Sharp_Programming/Lexing_and_Parsing>
   (e) Scala：Scala 解析组合子
     - <https://github.com/scala/scala-parser-combinators>
   (f) ANTLR
     - <https://www.antlr.org/about.html>
   这些工具很方便，但手写词法分析器和解析器也很有乐趣！
   (a) 关于在 Scala 中手写解析生成器的教程：《Scala 中的函数式编程》第 9 章 [17]。
5. LLVM
   (a) Kaleidoscope 教程：<https://llvm.org/docs/tutorial/index.html>
   (b) LLVM 文档首页：<https://llvm.org/docs/>
   (c) 面向研究生的 LLVM：<https://www.cs.cornell.edu/~asampson/blog/llvm.html>
   特别说明：如大家所知，LLVM 确实不太方便。而且它的 API 缺乏向后兼容。
   除 C/C++ 外，LLVM 还有对 OCaml、Haskell、Rust、Go、C#、F#、Node.js、Python 的绑定。
6. 一些有趣的开源编译器相关项目：
   (a) Halide/TVM
   (b) TACO
   (c) LLVM/MLIR
   (d) XLA
   (e) QEMU
7. 先修知识：
   - 必修：
     (a) 计算机体系结构：ILP（指令级并行）、存储层次
       i. 只有当你想学编译器优化时这才是必修。
   - 推荐：
     (a) 理论计算机科学（TCS）
       i. 《计算理论导引》（第 3 版）[55]
         - 第 1、2 章足够。对编译器，会用这些自动机就够了。不必担心证明。
     (b) 计算机体系结构：DLP（数据级并行）、TLP（线程级并行）
     (c) 操作系统：线程、上下文切换
   - **程序设计语言（PL）**
     - Java。

## 6 程序设计语言（Programming Languages, PL）

谈 PL 时，我们实际在谈两件事：

- 编程（programming）
- 验证（verification）

缩写：

- OOP：面向对象编程
- FP：函数式编程

### 6.1 语言清单

#### 6.1.1 程序设计语言清单

**学习顺序建议：**

1. 从函数式语言开始，因为它们不需要考虑内存——内存对新手总是令人困惑且容易出错。而且，函数式编程让你更关注计算的描述而非其实现；这真是件幸事。
2. 选哪种函数式语言？
   (a) Lisp 家族太陈旧过时。
   (b) 像 Haskell 这样的纯函数式语言也不合适。想想理解 monad 需要付出的努力！
   (c) Scala 也不太好，因为它复杂、虽然现代。
   (d) 剩下真正的选择是 ML 家族，其中 OCaml 和 F# 都很好。F# 更现代易学；OCaml 更成熟。
   (e) 不过，从 ML 家族起步听起来有点可怕。
   (f) 考虑先学 Kotlin，因为它简单现代，除了缺乏对模式匹配的完整函数式支持外，已经足够函数式。
3. 有了 Kotlin 和 OCaml/F# 的基础后，几乎可以轻松学会所有主流流语言，如 Java、TypeScript、Scala（尽管这个显然比前两个需要更多努力）；此外你还可以向 Rust 前进（耗时！），再往后是传奇的 C++。如果 Rust 对你太难，就先学 Go。

**技巧（Tips）：**

1. 选择 IDE 的一般技巧：
   (a) 对运行在 JVM 上的语言，选 JetBrains。
   (b) 如果 JetBrains 有针对你目标语言的专用软件，优先用它。
   (c) 否则，VS Code 总是好选择。
   这里列出的我用过的 IDE 只是这里提一下，可能还有其他优秀 IDE。
2. 给 Windows 用户选择平台的一般技巧：
   (a) 对 .NET 上的语言，Windows 显然是最佳。
   (b) 否则，WSL2 至少不比 Windows 差。
   (c) 对 C/C++、OCaml 这类老式 AOT（提前编译）语言，Windows 可能是灾难（很多兼容性问题）。
   (d) 对 JIT（即时编译）语言和现代 AOT 语言如 Go、Rust，选哪个都无所谓（在 Windows 上用 Haskell 也没问题）。
   (e) Python 是特例，某些包在 Windows 上兼容性不够好。
3. 开发工具链模型。你不仅需要编译器、库和 IDE，还需要构建工具、调试器、测试工具、linter，甚至 sanitizer、profiler、formatter 等。
4. 框架是 PL 生态系统的关键组成。某门 PL 的成功高度依赖其框架。
5. 有时在教程/文档中搜索比 Google 给出更好的答案。
6. 除非明确指定，永远用最新版本。

- **C/C++**（请学 C++ 的最新版，或至少 C++17）
  如果可能，先学 Rust。
  - 教程
    1. 《C 程序设计语言》（第 2 版）[50]
       - "K&R"
    2. 《C++ 程序设计语言》（第 4 版）[60]
  - 文档
    1. <https://cppreference.com/>
    2. Boost C++ 库：<https://www.boost.org/>
       - 有时标准 C++ 库不够用。这种情况下 Boost 可能提供有用的额外功能。此外，Boost 的一些功能可能在未来并入标准 C++ 库，一如往常。
  - 编程指南
    - Scott Meyers 的"Effective C++"书系
      - Effective C++（第 3 版）[36]
      - Effective Modern C++（第 1 版）[37]
      - Effective STL（第 1 版）[35]
    - C++ Core Guidelines：<https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines>
  - 推荐 IDE：Linux 上的 VSCode（特别是 WSL）。
  - 推荐编译器：最新版 GCC 和 Clang。
    - 目前，Clang 13 的 OpenMP 支持需要单独安装，Clang 12 则不必。
    - GCC 可从源码构建：源码地址 <https://github.com/gcc-mirror/gcc/tags>。
    - Clang 可直接从 <https://releases.llvm.org/download.html> 下载。
  - 构建工具：
    - CMake（CUDA 也可用）：CMake 教程 <https://cmake.org/cmake/help/latest/guide/tutorial/>
    - GNU make：<https://www.gnu.org/software/make/manual/make.html>
  - GoogleTest 用户指南：<https://google.github.io/googletest/>
  - Linter：Clang-Tidy：<https://clang.llvm.org/extra/clang-tidy/>
    - C/C++ 的编码风格比其他语言更重要，因为这门语言的历史包袱、灵活性和安全问题。
  - IDE 设置指南：
    1. VSCode。Windows 用户选 WSL。
    2. 最新 G++/Clang++。
    3. VSCode 扩展：Clangd。
    4. 两个文件：.clang-format、.clang-tidy。
    5. compiledb（确保智能提示工作）。
    6. Makefile（可由 CMake 生成）。

- **Java**（建议用 Java 17 或至少选一个 LTS 版本）
  考虑先学 Kotlin。
  先修语言：无。
  注意与 C++、以及 JVM 和 JIT 的比较。
  - 教程
    1. Oracle 在线教程：<https://docs.oracle.com/javase/tutorial/>
    2. Core Java（第 10 版）。两卷：
       - 卷 I：基础 [24]
       - 卷 II：高级特性 [61]
  - 文档
    1. <https://docs.oracle.com/javase/specs/>
  - 编程指南
    - Effective Java（第 3 版）[13]
  - GraalVM：<https://www.graalvm.org/>
  - 推荐 IDE：IntelliJ Idea
  - 构建工具（适用于 JVM 上所有语言）：Maven 或 Gradle。
    - Maven in 5 Minutes：<https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html>
    - 所有文档见：<https://maven.apache.org/>
    - 试试 IntelliJ Idea 中的 Maven。
  - Spring：<https://spring.io/quickstart>

- **C#**
  为了学习，C# 是 Java 的（好得多的）替代品，也是进入 .NET 生态系统的钥匙。
  1. Microsoft C# 文档：<https://learn.microsoft.com/en-us/dotnet/csharp/>

- **Scala**（Scala 3 已出！）
  Scala 比 OCaml 更多地借鉴 Haskell。
  先修语言：无（如果你觉得 Scala 太难学，先试 Kotlin）。
  显著特性：FP。
  像 Scala、OCaml、F# 这样的多范式语言是很好的起点，因为你的编程风格可以从命令式编程逐步过渡到函数式编程。
  - 教程
    1. Tour of Scala：<https://docs.scala-lang.org/tour/tour-of-scala.html>
    2. Scala Book：<https://docs.scala-lang.org/overviews/scala-book/introduction.html>
  - 文档
    - Guides and Overviews：<https://docs.scala-lang.org/overviews/index.html>
    - 所有文档：<https://docs.scala-lang.org/>
      - Scala 3 文档也可在那里找到！
  - 推荐 IDE 与构建工具：同 Java。
  - 学 PL，用 Scala 3。为生态系统起见，目前更推荐 Scala 2。

- **Kotlin**
  在我看来，它是入门级程序员的最佳语言。
  先修语言：无。
  一起试 Scala 和 Kotlin。
  显著特性：null 安全，适度的 FP。
  - 教程
    1. Get started with Kotlin：<https://kotlinlang.org/docs/getting-started.html>
    2. Kotlin Coroutines：<https://github.com/Kotlin/KEEP/blob/master/proposals/coroutines.md>
       - 关于栈less 协程设计的精彩文章！
  - 文档
    1. <https://kotlinlang.org/docs/>
  - 推荐 IDE 与构建工具：同 Java。

- **Go**（Go 1.18，带泛型已出！）
  先修语言：无。
  显著特性：并发编程（goroutine + channel + 异步，GMP 模型），适度的 OOP（与 Java 的 OOP 相比）。
  - 教程
    1. A Tour of Go：<https://go.dev/tour/welcome/1>
    2. Effective Go：<https://go.dev/doc/effective_go>
    3. 官方教程（含泛型、fuzzing 和关系数据库访问）：<https://go.dev/doc/tutorial/>
  - 文档
    1. 所有文档见：<https://go.dev/doc/>
  - 博客
    - The Go Blog：<https://go.dev/blog/>
      - 关于 Go 设计的精彩文章！例如《Getting to Go: The Journey of Go's Garbage Collector》：<https://go.dev/blog/ismmkeynote>
    - Russ Cox 的博客：<https://research.swtch.com/>
      - 不仅有很多 Go 相关博客，还有其他有趣话题！
  - 推荐 IDE：GoLand、VSCode
  - 构建工具：<https://go.dev/doc/modules/gomod-ref>

- **Rust**
  一门极高性能、内存安全、无垃圾回收的语言。
  Rust 的大多数特性可在 C++ 或 OCaml 中找到；理解这两门语言能帮你理解 Rust。
  先学 C++ 还是 Rust？由于 C++ 的流行，大多数人在听说 Rust 之前就接触过它。然而，Rust 的设计更一致、更整洁、更少被误用，也没有 C++ 那些可怕的历史包袱。因此我认为值得先学 Rust 再学 C++。
  - 教程
    1. The Rust Programming Language：<https://doc.rust-lang.org/book/>
       - 也是关于编程语言设计的一本好书！
    2. Rust By Example：<https://doc.rust-lang.org/stable/rust-by-example/>
    3. 异步 Rust：<https://rust-lang.github.io/async-book/>
    4. The Rustonomicon：<https://doc.rust-lang.org/nomicon/>
       - 这本书讲"不安全"。
  - 课程
    1. CS 110L 系统中 Rust 安全编程：<https://web.stanford.edu/class/cs110l/>
  - 文档
    1. The Rust Reference：<https://doc.rust-lang.org/reference/>
    2. <https://doc.rust-lang.org/beta/>
  - 很多优秀书籍见：<https://www.rust-lang.org/learn>
  - 推荐 IDE：VSCode、IntelliJ Idea
    - 我个人更喜欢 VSCode，因为它的分析器运行更快、类型推断做得更好。
  - 一些不错的 crate（Rust 的包名）：
    1. 线程级并行：rayon。
    2. 异步编程：futures + tokio/async-std/smol。
  - 构建工具：Cargo。
    - The Cargo Book：<https://doc.rust-lang.org/cargo/>
    - 其教程也可在《Rust 程序设计语言》中找到。

- **OCaml**（OCaml 5.0，已支持多核！）
  ML 是 OCaml 的祖先，这门编程语言为其创造者赢得了图灵奖，因为它是"第一门包含多态类型推断和类型异常处理机制的语言"。
  先修语言：无。
  熟悉 Scala 会很有帮助。
  与 Scala 比较：
  1. Scala 更像是命令式编程与函数式编程的混合；而 OCaml 中函数式编程为主、命令式编程为辅。
  2. OCaml 的类型推断比 Scala 更强大。例如在 Scala 中，递归函数需要显式指定函数参数和返回类型。
  3. Scala 允许隐式转换，这在 OCaml 中几乎不可能。OCaml 的类型系统相当严格。
  如果你学过其中任一门，我强烈建议你学另一门。
  - 教程：
    1. Real World OCaml：<https://dev.realworldocaml.org/>
       - OCaml 是少数几个在性能上极其重视性能的 PL，尤其在函数式语言中幸运的是，这本书给出了 OCaml 实现的介绍，特别是时间和空间开销。这些内容很有教育意义，因为函数式程序员往往对这些了解不多。
       - 这本书由 Jane Street 的人撰写，因此偏向实践而非理论数学/你期待的 FP 书籍那样。
    2. The OCaml Manual：<https://v2.ocaml.org/manual/index.html>
    3. 官方入门教程和文档：<https://ocaml.org/docs>
  - 课程：
    - Cornell CS 3110 用 OCaml 的函数式编程：<https://cs3110.github.io/textbook/cover.html>
    - 哈佛 CS 51 计算的抽象与设计：<https://cs51.io/>
  - 构建工具：dune。
    - <https://dune.readthedocs.io/en/stable/>
  - 包管理器与版本管理工具：opam。
  - 推荐 IDE：VSCode
  - 注意：
    1. Windows 用户请考虑用 WSL2 跑 OCaml。

- **F#**
  F# 与 OCaml 非常相似，运行在 .NET 平台上。由于二者相似，一旦你掌握其中一门，再学另一门就很容易。
  先学哪个？OCaml 还是 F#？
  两者都是好选择。对新手，它们互为不错的替代。F# 更现代、更难学、且摆脱了 OCaml 的语法。
  - 教程
    1. Beginning F#（视频系列）：<https://www.youtube.com/playlist?list=PLdo4fOcmZ0oUFghYOo89baYBTGXUkC7Z>
    2. F# for Fun and Profit：<https://fsharpforfunandprofit.com/site-contents/>
    3. F# 语言指南：<https://learn.microsoft.com/en-us/dotnet/fsharp/language-reference/>
  - 其他学习材料
    1. F# Software Foundation：<https://fsharp.org/learn/>
    2. Microsoft：<https://dotnet.microsoft.com/en-us/learn/fsharp>
  - 文档
    1. F# 文档：<https://docs.microsoft.com/en-us/dotnet/fsharp/>
  - F# 对异步和并发编程有良好支持：
    - async：<https://learn.microsoft.com/en-us/dotnet/fsharp/tutorials/async>
    - task：<https://learn.microsoft.com/en-us/dotnet/fsharp/language-reference/task-expressions>
    - MailboxProcessor（actor 模型）：<https://fsharpforfunandprofit.com/posts/concurrency-actor-model/>
  - 推荐 IDE：VSCode

- **Haskell**
  推荐用 GHC。
  纯函数式语言。
  显著特性：
  1. 纯度 & 惰性
  2. 类型类 & 类型系统
  3. monad & 代数设计
  懂一点程序语言理论会有帮助。我个人直到学完斯坦福 CS 242 才理解一些最优雅的设计。
  了解一点抽象代数对学习 Haskell 中的代数设计很有帮助。
  先修语言：无。
  推荐学习顺序：OCaml/F# → Scala → Haskell。
  OCaml 与 Haskell 的关键区别：
  1. 纯度。
  2. 惰性。
  3. Haskell 有远更复杂高级的类型系统，而 OCaml 有更复杂的模块系统。
  Haskell 以陡峭的学习曲线著称，合适的学习顺序能为你征服它提供足够基础。
  - 教程
    1. Learn You a Haskell for Great Good!：<http://learnyouahaskell.com/chapters>
       - 对新手，这本比 Real World Haskell 好。
    2. Real World Haskell：<http://book.realworldhaskell.org/read/>
    3. Wikibooks 为有经验的 Haskell 程序员提供了不错的教程和高级主题：<https://en.wikibooks.org/wiki/Haskell>
    4. HaskellWiki 真的很有用。
  - 所有书籍、课程、教程、文档和各种资源见：<https://www.haskell.org/documentation/>
  - 常用网站：
    - Hackage
    - HaskellWiki
    - Wikibook
    - Hoogle
  - GHC 用户指南：<https://downloads.haskell.org/~ghc/latest/docs/users_guide/>
    - GHC 有很多重要扩展，都可在这里找到。
  - 工具链管理工具：GHCup
    - 不要把你机器上的 GHC 版本与 ghcup 外部的版本搞混！
    - 为使 VSCode 使用 stack 中指定的 GHC 版本工作，该特定版本必须与 Haskell Language Server 支持的 GHC 版本兼容，而它应安装在 GHCup 内；不必把它设为默认。此外，打开项目时的初始化延迟相当大，因此需要耐心。
  - 构建工具：
    - Stack（推荐）：<https://docs.haskellstack.org/en/stable/>
      - 大多数时候你只需对付 stack。
    - Cabal（不推荐）：<https://www.haskell.org/cabal/>
  - Haskell 的类型系统是个好例子。关于它的好文章：<https://en.wikibooks.org/wiki/Haskell/The_Curry%E2%80%93Howard_isomorphism>（即"Curry–Howard 同构"，及其后 value/type 那一套）。
  - A History of Haskell：<https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/history.pdf>
  - 推荐 IDE：VSCode
  - 注意：
    1. Windows 用户请考虑用 WSL2 跑 OCaml。

- **JavaScript/TypeScript/AssemblyScript**
  先修语言：无。
  TypeScript 相比 JavaScript 的改进值得学习。
  注意它的异步编程技术：
  1. 回调（callback）
  2. Promise（async）、await。
  - 教程
    1. W3Schools JavaScript 教程：<https://www.w3schools.com/js/>
    2. Mozilla Web Docs 中的 JavaScript：<https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide>
    3. W3Schools TypeScript 教程：<https://www.w3schools.com/typescript/>
    4. TypeScript 手册：<https://www.typescriptlang.org/docs/handbook/intro.html>
    5. Node.js 官方教程：<https://nodejs.dev/learn>
    6. The AssemblyScript Book：<https://www.assemblyscript.org/introduction.html>
  - 书籍
    1. JavaScript: The Good Parts [20]
  - 文档
    - JavaScript：MDN Web Docs
    - TypeScript 文档：<https://www.typescriptlang.org/docs/>
  - 推荐 IDE：VSCode
  - 与 WASM 相关的资源见 [18]。

- **Swift**
  1. 官方文档：<https://www.swift.org/documentation/>

- **Julia**
  易学、易写、高性能。
  一门适用于科学计算和快速原型的好语言，原生支持 GPU 编程和分布式编程，并良好支持即时编译（JIT）和渐变类型。
  不要过度使用它；我认为它不适合大型项目。
  1. 官方文档：<https://docs.julialang.org/en/v1/>

#### 6.1.2 定理证明器清单

1. **Lean**
   主要是一个定理证明器，也是一门编程语言（尽管不像专门为编程设计的语言那样好用）。
   (a) Lean 官方文档：<https://leanprover.github.io/about/>
   (b) 推荐 IDE：VSCode
   (c) Lean 教程：<https://leanprover.github.io/theorem_proving_in_lean/>
   (d) 版本管理工具：elan
   (e) 推荐 IDE：VSCode
2. **Coq**
   基于 OCaml。
   - <https://coq.inria.fr/>
3. **Agda**
   基于 Haskell。
   - <https://wiki.portal.chalmers.se/agda/pmwiki.php>

#### 6.1.3 其他语言

PL 与库之间没有清晰界限。因此，很多库可被视为领域特定语言（DSL），从而被推荐如下。
还有一些其他语言值得注意甚至学习。它们属于不同编程范式，在编程语言史上有重要影响。

**数组编程：APL、K**
- Numpy 可视为它们的现代后裔。一些从 Numpy 衍生的 DSL，如 PyTorch 和 JAX，也是好选择。

**逻辑编程：Prolog、Datalog、Epilog**

**张量代数**
- 稠密张量代数：Halide、TVM
- 稀疏张量代数：TACO（<http://tensor-compiler.org/>）

#### 6.1.4 古老的函数式语言

- Lisp 方言：Racket

**可满足性模理论（SMT）求解器**
- Z3、CVC5

**数学家语言：Mathematica**

### 6.2 函数式编程（Functional Programming）

- 书籍
  - 推荐给初学者
    这些书不仅教 FP 的**语法**，（更重要地）还教如何以函数式风格设计软件，以及这些函数特性的背景和由来。
    1. 《计算机程序的构造和解释》（第 2 版）[1] / JavaScript 版 [2]
       - 原版基于 **Scheme**（Lisp 方言）。不过 Lisp 及其方言现在都过时了。但这本书仍然非常值得推荐。
       - 这本书的意义远超教我们函数式编程。
    2. 《Scala 函数式编程》[17]
       - 第 1 版基于 Scala 2，第 2 版基于 Scala 3。除这两版外，这两个版本基本相同。
  - 纯函数式数据结构 [40]
  - 其他书籍
    1. 《Java 8 函数式编程实战：Lambda、Stream 与函数式风格编程》（第 1 版）[62]
    2. 所有关于 Haskell 和 OCaml 的书。
- 建议的语言学习顺序：
  1. 从 OCaml/F# 开始。这是最干净的。我个人觉得 F# 更好。
  2. 进阶到 Scala。它特性更多、范式更多，比 OCaml/F# 更难学、更容易混淆。不过，Scala 中 trait（类型类）对学习函数式设计很有帮助，而 F# 中缺失它（尽管可以用模块模拟 F# 中的 trait）。此外，既然 Scala 源自 Haskell，学它有助于你学 Haskell。
  3. 这时可以试一些像 Rust 这样有大量函数特性的语言。
  4. 然后你可以用传奇的 Haskell 挑战自己了。如果你对这些东西的基础足够扎实，学这门语言就不会那么可怕。从编程语言理论角度，它确实拥有一些不错的性质，如 termination（若评估序导致终止，则会终止）。

### 6.3 程序设计语言理论（Programming Languages Theory）

它不仅关于编程，也关于验证。

- 课程
  - 斯坦福 CS 242 程序设计语言：
    - Will Crichton：<https://stanford-cs242.github.io/f19/>（更实用、更多开放源码材料，如讲义和作业）
      - 所用语言：OCaml、WASM、Rust
    - Alex Aiken：<https://web.stanford.edu/class/cs242/materials.html>（更理论、更全面深入）
      - 建议在本课前先学的语言：OCaml、Haskell、Rust
      - 所用语言：
        1. C++、Java：主流 OOP 语言
        2. OCaml、Haskell：静态类型函数式语言；Haskell 中的 monad
        3. Python、JavaScript：动态类型语言
        4. Rust：ownership（实现类型抽象）
        5. Racket：call/cc 来使用 continuation
        6. Lean：定理证明器
        7. NumPy：带组合子的数组编程
      - 其他有助于理解背景的语言：
        1. Go：channel
        2. TypeScript：渐变类型
        3. Kotlin：coroutine
        4. Scala：支持大多数 OOP 和 FP 特性的复杂类型系统
      - 先修知识：
        - 必修：
          1. 命题逻辑
          2. 函数式编程
        - 推荐：
          1. 编译器
          2. 编程语言实现
        - 弱推荐：
          1. 操作系统
          2. 计算机体系结构
          3. 理论计算机科学
      - 本课程背景极深，因此对计算机科学（尤其是不同范式的编程语言）有透彻理解会带来很大不同。
  - 斯坦福 CS 151 逻辑编程：<http://logicprogramming.stanford.edu/stanford/lessons.php>
- 书籍
  1. 《程序设计语言基础》[38]
  2. 《类型与程序设计语言》（第 1 版）[47]
     - 基于 OCaml。
  3. 《类型与程序设计语言高级专题》（第 1 版）[48]
  4. 《程序设计语言实践基础》（第 2 版）[25]
- 先修知识：
  - 必修：
    1. 一门 OOP 语言（Java 可以，但 C++/Python 不够），一门 FP 语言。基础知识足够。
       - 个人推荐 Scala/OCaml/F#（我个人觉得 F# 最好）+ Rust。它们几乎涵盖现代常用编程语言的所有范式。
  - 推荐：
    1. 计算机体系结构
    2. 编译器
    3. 操作系统

**建议（Suggestions）**

- 不必一次掌握一整门 PL；而是需要时学一部分。
- PL 发展迅速。为跟上最新发展，除书籍外参考在线文档/教程/博客。
- 下列每个范式至少掌握一门现代语言：
  - 过程式（Procedural）
  - 面向对象（Object-Oriented）
  - 函数式（Functional）
  注意，像 Go、Scala、Kotlin、Rust 这样的现代语言可能与 Java、Python 这样的老语言大不相同。特别地，尽管现代 C++（C++11 及以后）真的很现代，但不可避免地有大量历史包袱，所以 C++ 可视为一个混合物。
- PL 至少可从三个视角看：
  - 计算机系统
  - 软件工程
  - 软件理论
    - 例如，编程范式与 Church–Turing 论题的关系。
  因此，你总能在 PL 中找到大量交叉问题。
- 完整的编程范式清单：<https://en.wikipedia.org/wiki/Programming_paradigm>
- 注意三类安全：
  - 类型安全
  - 内存安全
  - 线程安全
- 注意每种语言的内存一致性模型（在此上下文常称内存模型），尽管这对应用层编程几乎没有影响。
- 具体例子对理解抽象概念总是大有帮助，这也是为什么你应该精通几门语言。
- 注意某门语言与 C/C++（以及 JVM 上的 Java）之间的互操作。

## 7 并行计算（Parallel Computing）

并行计算由三部分组成：

- 体系结构（系统）
- 编程（应用）
- 算法（理论）

并行计算是计算机体系结构的自然延伸。

**特别注意：**

- 投身此部分之前先读《计算机体系结构：量化研究方法》（CAAQA），在有了并行计算的实际经验后再回头重读这部杰作！
- 不做内存优化的并行计算是可笑的！
- 学习如何分析性能瓶颈——这对并行程序的成功至关重要。具备计算机体系结构和操作系统的知识会极有帮助。
- 并行计算应包含分布式计算；但本节不涉及后者。

### 7.1 平台（Platforms）

- **CUDA**（类别：逻辑上数据并行，GPU）
  - 《CUDA 示例》（第 1 版）[53]
    - 有点过时，但思想讲得很好。如果你基础够好，直接看下面两份文档即可，这两份强烈推荐。
  - CUDA C++ 编程指南：<https://docs.nvidia.com/cuda/cuda-c-programming-guide/>
  - CUDA C++ 最佳实践指南：<https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/>
  - Thrust：<https://docs.nvidia.com/cuda/thrust/index.html>
    - CUDA 中的 STL，提供一些高层抽象。
  - 所有文档见：<https://docs.nvidia.com/cuda/>
  CUDA 对异步编程和异构编程也极好！你也可以借由 CUDA 体验计算！
- **Intel ISPC**（类别：逻辑上数据并行，CPU）
  - Intel ISPC 用户指南：<https://ispc.github.io/>
- **CPU intrinsics**（类别：逻辑上数据并行，CPU）
  - x86 intrinsics（类别：DLP，多媒体 SIMD 指令集扩展）
    - <https://www.intel.com/content/www/us/en/docs/intrinsics-guide/index.html>
  - ARM SVE2 intrinsics（类别：DLP，向量体系结构）
    - <https://developer.arm.com/documentation/102340/0001/Program-with-SVE2>
  - ARM Neon intrinsics（类别：DLP，多媒体 SIMD 指令集扩展）
    - <https://developer.arm.com/documentation/102467/0100/Why-Neon-Intrinsics->
- **MPI**（类别：逻辑上任务并行，消息传递）
  - MPI 教程：<https://mpitutorial.com/tutorials/>
  - YouTube 视频
    - MPI Basics：<https://www.youtube.com/watch?v=c0C9mnQaxsD4>
    - MPI Advanced：<https://www.youtube.com/watch?v=q9OfXis50Rg>
- **OpenMP**（类别：逻辑上数据并行，共享内存）
  - Tim Mattson（Intel）在 YouTube 上的《OpenMP 简介》（2013）
    - 视频：<https://www.youtube.com/playlist?list=PLLX-Q6B8xqZ8n8bwjGdzBJ25X2utwnoEG>
    - 幻灯片：<https://www.openmp.org/wp-content/uploads/Intro_To_OpenMP_Mattson.pdf>
  熟悉 pthread 的人学 OpenMP 相当容易。
- **高级 DSL**
  1. PyTorch
     - PyTorch 2.0 已发布！
     - 官方站点 <https://pytorch.org/> 提供足够高质量的学习资源。
  2. JAX：<https://jax.readthedocs.io/en/latest/>

### 7.2 类别（Categories）

并行计算的本质是缺乏依赖。

- **ILP（指令级并行）**
  ILP 的数学模型——DAG（有向无环图）：
  - 节点：一条指令的一个阶段。
  - 边：依赖（数据依赖、控制依赖、名字依赖），存在于一对节点之间。
  目标：消除依赖（边），利用节点间缺乏依赖。
- **DLP（数据级并行）**
  DLP 编程的本质：向量化（Vectorization）。
  - 要动手体验，可以从 PyTorch 开始，因为它让你摆脱低层细节，同时保留元素和存储层次。
    - 官方教程：<https://pytorch.org/tutorials/>
    - 此外，PyTorch 是利用 GPU 做并行计算的便捷工具。
- **TLP（线程级并行）**
  TLP 编程的本质：异步（并发控制流）、await（同步）。
  - 并发机制
    1. Thread：几乎所有主流语言都支持，如 C++ 的 std::thread/jthread、Java、pthread。
    2. Future/Promise：大多数主流语言支持，如 Scala、C++、Java。
    3. Stackful Coroutine：Go、Haskell。
    4. Stackless Coroutine：Kotlin、Rust（async/await）、F#（async/task）、Haskell。
  - 附：
    1. 这里是 Kotlin 教程中提供的异步编程技术的好总结：<https://kotlinlang.org/docs/async-programming.html>
    2. 异步编程的本质是 async/await 以及挂起点。
       - 对线程和栈ful 协程，每个点都是挂起点，而对栈less 协程，只有一小部分函数是挂起点且显式声明。
    3. 对各实现，搞清楚什么是"continuation"，以及它在进程、线程、栈ful 协程、栈less 协程之间如何变化。还要思考 continuation 与挂起点的关系。
  - 同步机制
    - 共享内存
      1. Mutex、条件变量：大多数语言。
      2. Monitor：Java。对 C++，可用 RALL 方便地模拟。
      3. 原子变量/操作：大多数语言。
      4. Barrier：大多数语言，尤其在 CUDA 这类数据并行编程中。
      5. 读写锁：大多数语言。
      6. 软件事务内存：Haskell。
      很多广泛使用的机制未列出。
    - 消息传递
      1. Channel + Select：Go、Kotlin。
      2. Actor 模型：
         - Akka（带 Java/Scala 接口）：<https://doc.akka.io/docs/akka/current/typed/guide/introduction.html>
         - Kotlin：<https://kotlinlang.org/docs/shared-mutable-state-and-concurrency.html#actors>
         - F# MailboxProcessor：<https://fsharpforfunandprofit.com/posts/concurrency-actor-model/>
    - 高级封装
      1. 线程安全集合
         - Java：java.util.concurrent：<https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/concurrent/package-summary.html>
  - 附——并发、并行、异步的比较：
    1. 并发：多个计算在重叠时间段内执行。
    2. 并行：多个计算在同一时刻运行，或单个计算的多个部分同时运行。
    3. 异步：当一个或多个计算可与主程序流分开执行时。
    （来源：<https://docs.microsoft.com/en-us/dotnet/fsharp/tutorials/async>）

### 7.3 并行计算原理

- 斯坦福 CS 149 并行计算：<https://gfx.stanford.edu/courses/cs149/fall21/>
  - 所用编程语言和平台：
    1. C++ and std::thread
    2. ISPC
    3. CUDA
    4. OpenMP
    5. AVX intrinsics
- 斯坦福 CS315B 并行编程：<https://web.stanford.edu/class/cs315b/>
- 斯坦福 CME 323 分布式算法与优化：<https://stanford.edu/~rezab/classes/cme323/S20/>

**先修知识：**

- 必修：
  1. 计算机体系结构
- 推荐：
  1. 函数式编程（强烈推荐）
  2. 操作系统
  3. 编译器

### 7.4 内存模型（Memory Model）

它也称"内存一致性模型"或有时"内存序"。

在我看来，这是并发编程中最棘手的部分。
这是一个交叉问题，涉及以下领域：

1. 计算机体系结构：内存一致性
2. 并发编程：无锁编程
3. 编译器：重排序（包括代码调度、投机、部分冗余消除、公共子表达式消除、拷贝传播、冗余读写消除等）、寄存器分配。

这个问题出现在以下场景：

1. 无锁编程
2. 编译器开发
3. 并发相关库的开发
4. OS 开发

以 C++ 为例，涉及以下内容：

1. 内存序（作为下列函数/方法的参数传入）
2. atomic
3. atomic thread fence
4. atomic signal fence（编译器 fence）

主流 PL 的内存模型可分为几类：

1. C++、Rust、Go
2. Java
3. OCaml

具体描述可在各自官方文档中找到。值得一读，但对新手不够友好。下面是一些对新手更友好的资源：

1. Preshing 关于 C++ 的博客：<https://preshing.com/20120913/acquire-and-release-semantics/>
   - 他博客里有很多相关文章，我强烈推荐！
2. Rust Atomics and Locks：<https://marabos.nl/atomics/preface.html>
   - 第 2、3、7 章。
3. Java 内存模型：<http://www.cs.umd.edu/~pugh/java/memoryModel/>

还有一些论文值得读：

1. Boehm 关于 C++ 内存模型的论文：
   (a) 《线程无法作为库实现》：<https://www.hpl.hp.com/techreports/2004/HPL-2004-209.pdf>
   (b) C++ 并发模型基础：<https://www.hpl.hp.com/techreports/2008/HPL-2008-56.pdf>
2. Java 内存模型：<https://rsim.cs.uiuc.edu/Pubs/popl05.pdf>
3. 《在空间和时间上界定竞态》（针对 OCaml 内存模型）：<https://dl.acm.org/doi/pdf/10.1145/3192366.3192421>

**技巧：**

1. Compiler Explorer（<https://godbolt.org/>）会是你的好朋友。
2. 试试不同的 PL 和 ISA！
3. 有时需要参考 ISA 规范。

## 8 异步编程（Asynchronous Programming）

**注意**

并行计算解决的是计算密集型程序的性能工程，而异步编程处理的是 I/O 密集型程序的性能工程，后者通常比前者更难。

### 8.1 编程语言中的异步支持

#### 8.1.1 异步框架

有两种风味：

1. **Stackful 协程（Stackful Coroutines）**
   也称用户线程或绿色线程。它们的编程模型与内核线程相同。
   支持它的著名 PL 列表：
   (a) Java 21 虚拟线程。
   (b) Go goroutine。
2. **Stackless 协程（Stackless Coroutines）**
   这有时被直接称为 PL 手册/教程中的异步编程。
   通常这种编程范式涉及两个关键字：async、await。
   支持它的著名 PL 列表：
   (a) Rust 异步编程。
   (b) Kotlin 协程。
   (c) C#/F# 异步编程。
   (d) Python asyncio。
   (e) JavaScript
   (f) Swift 并发。
   (g) C++ 20 协程（尚未成熟）。

#### 8.1.2 异步操作支持

对异步操作（如异步 I/O、异步同步机制）的支持，也是 PL 异步编程生态系统的重要组成部分。我认为它是 PL 的一部分。
C#/F#、Rust、JavaScript 都很好，而 Kotlin（由于 JVM 缺乏异步）、Swift 目前还不支持。更糟的是，C++ 甚至没有一个一等网络库……

### 8.2 系统调用级别的异步支持

#### 8.2.1 非阻塞系统调用

- Socket 有良好支持，而常规文件通常没有。
- Linux man 手册页是好资源。

#### 8.2.2 I/O 多路复用

1. 反应式：select（已弃用）、poll（已弃用）、epoll
   - epoll 有两种模式：电平触发和边沿触发；都值得学：
   - 它们主要用于网络编程，对文件 I/O 效果差；
   - Linux man 手册页是这些系统调用的好资源。
2. 主动式：io_uring
   - io_uring 资料大全：<https://unixism.net/loti/>
   - 用 io_uring 做高效 I/O：<https://kernel.dk/io_uring.pdf>
   - 尽管（可以说）是 Linux 的未来，io_uring 仍处于早期阶段——不完整，有时行为不佳，相对各版本有巨大改进，有很多漏洞。
   - 手动安装的 liburing 可能与你的 OS 不兼容。
   - io_uring 提供真正的文件 I/O 异步（不是用线程池实现的）。
   - 我个人认为 io_uring 有深远意义。向 OS 请求服务不再需要系统调用。
   - io_uring 的两个关键思想：减少内核穿越和内存拷贝。

### 8.3 内核旁路技术（Kernel Bypassing Techniques）

这些需要硬件支持。

1. RDMA
2. DPDK
3. SPDK

我对这些了解不多。在此记录，希望有一天我能回来。

## 9 数据库（Databases, DB）

**特别注意**

- 思考 DB 与 OS 之间的关系（合作与冲突）。另外，当面对同样的问题（很多）如并发控制时，它们如何分别处理？
- 并行与分布式数据库和 NoSQL 是当今热点。请重点关注它们！
- 从全栈视角看 DB：从系统到应用再到理论（关系代数）。你在别处学的很多知识在这里起重要作用。此外，你也可以在这里找到大量交叉问题。
- 注意 DB 与大数据/数据挖掘之间的关系。

1. 书籍
   (a) 《数据库系统概念》（第 7 版）[54]
     - 划分：
       - 应用：第 2–11、25、26、28–32 章
       - 系统：第 12–24、32 章
       - 理论：第 2、27 章
     - 作为初学者，可先读 1–7、12–19 章。
     - 第 20–23 章：分布式系统的基础知识相当有帮助。详见下面"先修知识"。
     - 在第 10–11 章之后，在大数据/云计算方面获得一些经验后反思（如用 Spark 编程）。
     - 尽管第 3–5 章教了我们很多，而且确实有帮助，但如果你想学更多 SQL 规范，应参考下列手册，特别是那些特定于某 SQL 实现的。
     - CMU 15-445 和斯坦福 CS 145 基本都覆盖这本书。
     - 推荐在线章节：
       i. 第 27 章：形式化关系查询语言。覆盖：
          - A. 元组关系演算
          - B. 域关系演算
          - C. Datalog（一种基于逻辑编程语言 Prolog 的非过程查询语言）
       ii. 第 32 章：PostgreSQL。一个好的案例研究。
   (b) 补充
     i. 《数据库系统全本》[23]
2. 课程
   (a) DB 应用
     - 斯坦福 CS 145 数据管理与数据系统：<https://cs145-fa20.github.io/>
   (b) DB 系统
     - CMU 15-445/645 数据库系统导论：<https://15445.courses.cs.cmu.edu/fall2019/schedule.html>
     - 斯坦福 CS 245 数据密集系统原理：<https://web.stanford.edu/class/cs245/>
   (c) 高级 DB 系统
     - CMU 15-721 高级数据库系统：<https://15721.courses.cs.cmu.edu/spring2020/schedule.html>
3. 查询语言与平台
   - SQL
     - PostgreSQL
       (a) 数据库系统概念第 32 章：<https://db-book.com/online-chapters-dir/32.pdf>
       (b) 教程：<https://www.postgresqltutorial.com/>
       (c) 文档与手册：<https://www.postgresql.org/docs/>
     - MySQL
       (a) 教程：<https://www.mysqltutorial.org/>
       (b) 参考手册：<https://dev.mysql.com/doc/refman/8.0/en/>
     - 选哪个？
       (a) 它们是两个最流行的开源数据库。
       (b) 一般而言，由于历史原因 MySQL 仍更流行，而 PostgreSQL 更先进、更优雅。
       (c) MySQL 语法较怪，错误报告相对模糊甚至误导。
     - 特定数据库技巧：<https://db-book.com/university-lab-dir/db-tips.html>
   - NoSQL
     - MongoDB
       (a) Get Started：<https://www.mongodb.com/docs/guides/>
       (b) 文档：<https://www.mongodb.com/docs/>
     - Redis
       (a) <https://redis.io/>
     - Spark
       - Quick Start：<https://spark.apache.org/docs/latest/quick-start.html>
     - .NET LINQ
       - <https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/>
     - DB-Engines 排名：<https://db-engines.com/en/ranking>
       - 流行的数据库引擎排名和大量相关信息见这里。
     - 建议：
       (a) 学查询语言时，思考声明式编程（如 SQL）和逻辑编程（如 Datalog）。（附：逻辑编程是声明式编程的子集。）
4. 先修知识：
   - 必修：
     (a) 数据结构与算法：那些在二级存储上操作的尤其重要
     (b) 操作系统
   - 推荐：
     (a) 计算机体系结构
       - 在数据库中可找到很多类似想法（在计算机体系结构中）
     (b) 计算机网络
       - 学习并行与分布式数据库所需
     (c) 程序设计语言
       - 查询语言帮我们加深理解不同编程范式（如命令式 vs 声明式），以及一些可行但很少用的编程范式（如逻辑编程）。
   - 关于分布式系统的几句话
     - 很难决定下面两个先学哪个：并行与分布式数据库，还是分布式系统。我个人感觉这两个领域可以交错学习，因为你常需要在学习其中一个时参考另一个。作为一贯合理的方法，多次学习它们，这样你就不会错过重要先修知识，而最优学习顺序很难搞清。
   - **程序设计语言（PL）**
     - Java：JDBC。

## 10 分布式计算/分布式系统

1. MIT 6.824 分布式系统：<https://pdos.csail.mit.edu/6.824/schedule.html>
2. 补充
   (a) 普林斯顿 COS 418 分布式系统：<https://www.cs.princeton.edu/courses/archive/fall19/cos418/>
   (b) 斯坦福 CS 244B 分布式系统：<https://www.scs.stanford.edu/22sp-cs244b/>
   (c) 斯坦福 CS 251 加密货币与区块链技术：<https://cs251.stanford.edu/>
3. 先修知识：
   - 必修：
     (a) 操作系统
     (b) 计算机网络
     (c) 数据库
   - 推荐：
     (a) 计算机体系结构
     (b) 程序设计语言
       - 有一点函数式编程经验对学习分布式计算很有帮助。

## 11 云计算（Cloud Computing）

1. CMU 15-719 高级云计算：<https://www.cs.cmu.edu/~15719/old/spring2019/syllabus.html>
2. 斯坦福 CS349D 云计算技术：<http://web.stanford.edu/class/cs349d/>
3. 容器与容器管理系统
   (a) Docker
   (b) Kubernetes（K8s）
4. 先修知识：
   - 必修：
     (a) 操作系统
     (b) 计算机网络
     (c) 分布式系统
     (d) 数据库
5. 建议
   (a) 交叉问题很多。继续之前先确保满足先修。
   (b) 读关于 OS、计算机网络或计算机体系结构的前沿论文时，你可能遇到云计算问题。那时最好先有一些基础再读这些论文。

## 12 图形学（Graphics）

1. 斯坦福 CS 248A 计算机图形学：渲染、几何与图像操作：<https://cs248.stanford.edu>
2. 斯坦福 CS 348K 视觉计算系统：<https://cs348k.stanford.edu>
3. 只有上述与系统相关的课程被列出。其他图形课程请搜 CS *48（* 代表一位数字），任何后缀见 <https://explorecourses.stanford.edu/>。

## 13 大数据（Big Data）

1. 《设计数据密集型应用：可靠、可维护系统背后的大思想》（第 1 版）[31]
2. 先修知识：
   - 必修
     (a) 数据库
     (b) 分布式系统

## 14 软件工程（Software Engineering）

- 《人月神话：软件工程随笔》（周年纪念版）[15]
- 《设计模式：可复用面向对象软件的基础》[22]
  - 作者常被称为"四人帮（Gang of Four, GoF）"。
- 《软件设计哲学》（第 2 版）[41]
- 《代码大全 第 3 卷：软件工程》[30]
- 讨论最佳实践的材料也很有价值，见 **程序设计语言（PL）** 节，以及 CUDA 子节。

## 15 程序分析（Program Analysis）

广义上可视为编译器技术的一部分。

1. 软件基础：<https://softwarefoundations.cis.upenn.edu/>
   - 共 6 卷。
   - 卷 1 也教 Coq。
2. 先修知识：
   - 必修：
     (a) 编译器
     (b) 程序设计语言

## 16 计算机安全与密码学（Computer Security & Cryptography）

安全问题无处不在。新技术发明时就会出现新安全问题。
威胁模型因领域而异（如硬件 vs OS），导致不同技术。
编程语言内存安全的基础知识有帮助。

1. 教材
   (a) 《应用密码学研究生教程》：<http://toc.cryptobook.us/>
2. 课程
   (a) UC Berkeley CS 161 计算机安全：<https://sp22.cs161.org/>
   (b) 斯坦福 CS 155 计算机与网络安全：<https://cs155.stanford.edu/>
   (c) 斯坦福 CS 253 Web 安全：<https://web.stanford.edu/class/cs253/>
   (d) 斯坦福 CS 255 密码学导论：<https://crypto.stanford.edu/~dabo/cs255/>
   (e) 斯坦福 CS 350 安全编译：<https://theory.stanford.edu/~mp/imp/imp/mp-2019.html>
   (f) 斯坦福 CS 355 密码学高级专题：<https://cs355.stanford.edu/>
   (g) 斯坦福 CS 356 计算机与网络安全专题：<https://cs356.stanford.edu/>
3. Meltdown 和 Spectre：<https://meltdownattack.com/>
4. 先修知识：
   - 必修：
     (a) 操作系统
     (b) 计算机网络
     (c) （基础）概率论（密码学）
     (d) （基础）数论（密码学）
   - 推荐：
     (a) 计算机体系结构
     (b) 程序设计语言
     (c) 编译器
     (d) 数据库
   确实，在所有这些领域都能学到很多计算机安全知识。深入这些领域时特别注意安全问题。

## 17 Web

这些大多是应用层的东西。但这些内容频繁出现在现代计算机世界中，因此我加这一节以备不时之需。

1. 斯坦福 CS 142 Web 应用：<https://web.stanford.edu/class/cs142/index.html>
2. 斯坦福 CS 192X Web 编程基础：<https://web.stanford.edu/class/archive/cs/cs193x/cs193x.1176/lectures/>
3. 更多教程和参考见 W3Schools：<https://www.w3schools.com/>
4. 先修知识：
   - 推荐：
     (a) 操作系统
     (b) 计算机网络
     (c) 数据库

## 18 指令集体系结构（ISA）

下面的 ISA 都可以用 CSAPP 或《计算机组成与设计：硬件/软件接口》学习。不过下面的资源帮你走得更远。

- **x86**
  - Intel(R) 64 和 IA-32 体系结构软件开发者手册：<https://www.intel.com/content/www/us/en/developer/articles/technical/intel-sdm.html>
  - AMD 开发者指南和手册：<https://developer.amd.com/resources/developer-guides-manuals/>
  同时掌握"Intel"格式和"AT&T"格式。
- **RISC-V**
  - RISC-V 规范：<https://riscv.org/technical/specifications/>
    - 精彩的计算机体系结构书籍！
- **ARM**
  - ARM(R) CPU 体系结构关键文档：<https://developer.arm.com/architectures/cpu-architecture>
  - ARM 体系结构参考手册补充（Armv9-A 体系结构配置文件）：<https://developer.arm.com/documentation/ddi0608/latest>
- **PTX**
  - PTX ISA :: CUDA Toolkit 文档：<https://docs.nvidia.com/cuda/parallel-thread-execution/>
- **Java 字节码**
  - Java 语言与虚拟机规范：<https://docs.oracle.com/javase/specs/>
    - 点击"The Java Virtual Machine Specification"
  - Java 字节码指令列表（维基百科）：<https://en.wikipedia.org/wiki/List_of_Java_bytecode_instructions>
- **WebAssembly**
  严格说它不是 ISA，但它们有很多共同点，值得学习，所以我放在这里。
  - 官方网站：<https://webassembly.org/>
  - 规范：<https://webassembly.github.io/spec/core/index.html>
  - 用 WebAssembly 把 Web 提速：<https://people.mpi-sws.org/~rossberg/papers/Haas,%20Rossberg,%20Schuff,%20Titzer,%20Gohman,%20Wagner,%20Zakai,%20Bastien,%20Holman%20-%20Bringing%20the%20Web%20up%20to%20Speed%20with%20WebAssembly.pdf>

## 19 链接与加载（Linking and Loading）

1. 程序员的自我修养：链接、装载与库 [11]
2. 《链接器与加载器》（第 1 版）[33]
3. 建议
   (a) 不要只读关于 GCC/Clang 的书或文档。两者一起做。
   (b) 第一本书起主要作用，第二本是补充（不过我仍推荐读它）。
   (c) 这两本书相对过时（抱歉我没找到相关现代书）。此外第一本有不少学术错误。
   (d) 这两本书覆盖很多知识。挑你需要的章节。不必读每章。

## 20 工具（Tools）

1. Git
   - Git Magic：<http://www-cs-students.stanford.edu/~blynn/gitmagic/book.pdf>
   - GitHub 入门：<https://docs.github.com/en/get-started/quickstart/hello-world>
   - GitHub 文档：<https://docs.github.com>
   - 官方文档：<https://git-scm.com/doc>
   - 推荐 GitHub Desktop。
2. UNIX Makefile
   - Makefile 教程示例：<https://makefiletutorial.com/>
3. Docker
   - 官方教程与文档：<https://docs.docker.com/>
4. Shell 脚本
   - Shell Scripting 教程：<https://www.shellscript.sh/>
   - 下面两个教程基本相同，同一作者，前者对新手更友好：
     - Bash Scripting for Beginners 教程：<https://linuxconfig.org/bash-scripting-tutorial-for-beginners>
     - Bash Scripting 教程：<https://linuxconfig.org/bash-scripting-tutorial>
   - GNU Bash 手册：<https://www.gnu.org/software/bash/manual/>

## 21 编码风格（Coding Style）

- Google 风格指南：<https://google.github.io/styleguide/>
- Clang-Format 样式选项：<https://clang.llvm.org/docs/ClangFormatStyleOptions.html>
  - VS Code 可以不用装任何东西就用"clang-format"自动格式化代码！

## 22 杂项（Miscellany）

1. Intel(R) 产品规格：<https://ark.intel.com/>
2. GCC 在线文档：<https://gcc.gnu.org/onlinedocs/>
   - 优化选项：<https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html>
   - 选项汇总：<https://gcc.gnu.org/onlinedocs/gcc/Option-Summary.html>
   - 插桩汇总（含 sanitizer 和 profiler）：<https://gcc.gnu.org/onlinedocs/gcc/Instrumentation-Options.html>
3. GDB 文档：<https://www.sourceware.org/gdb/documentation/>
4. GNU 手册在线：<https://www.gnu.org/manual/>
5. Clang 12 文档：<https://releases.llvm.org/12.0.0/tools/clang/docs/index.html>
   - 改 URL 中的版本号即可获取其他版本文档。
6. LLVM 文档：<https://llvm.org/>
   - 很多出色的项目可在那里找到！

---

## 参考文献（References）

[1] H. Abelson 和 G. J. Sussman. *Structure and interpretation of computer programs*. MIT Press, 1996.
[2] H. Abelson, G. J. Sussman, M. Henz 和 T. Wright. *Structure and Interpretation of Computer Programs: JavaScript Edition*. MIT Press, 2022.
[3] A. Aho, M. Lam, R. Sethi, J. Ullman, K. Cooper, L. Torczon 和 S. Muchnick. *Compilers: Principles, techniques and tools*. 2007.
[4] T. Anderson 和 M. Dahlin. *Operating systems principles & practice volume ii: Concurrency*.
[5] T. Anderson 和 M. Dahlin. *Operating systems principles & practice volume iii: Memory management*.
[6] T. Anderson 和 M. Dahlin. *Operating systems principles & practice volume iv: Persistent storage*.
[7] T. Anderson 和 M. Dahlin. *Operating Systems Principles & Practice Volume I: Kernels and Processes*. Recursive books, 2014.
[8] A. W. Appel. *Modern Compiler Implementation in ML*. Cambridge University Press, 1998.
[9] A. W. Appel. *Modern compiler implementation in C*. Cambridge university press, 2004.
[10] A. W. Appel 和 J. Palsberg. *Modern compiler implementation in java*. 2003.
[11] 俞甲子, 石凡. 程序员的自我修养：链接、装载与库. 电子工业出版社, 2009.
[12] C. Benvenutti. *Understanding Linux network internals*. O'Reilly Media, Inc., 2006.
[13] J. Bloch. *Effective java (the java series)*. Prentice Hall PTR, 2008.
[14] D. P. Bovet 和 M. Cesati. *Understanding the Linux Kernel: from I/O ports to process management*. O'Reilly Media, Inc., 2005.
[15] F. P. Brooks Jr. *The mythical man-month: essays on software engineering*. Pearson Education, 1995.
[16] R. E. Bryant 和 D. R. O'Hallaron. Computer systems: A programmer's perspective, 2015.
[17] P. Chiusano 和 R. Bjarnason. *Functional programming in Scala*. Simon and Schuster, 2014.
[18] K. D. Cooper 和 L. Torczon. *Engineering a compiler*. Elsevier, 2011.
[19] T. H. Cormen, C. E. Leiserson, R. L. Rivest 和 C. Stein. *Introduction to algorithms*. MIT press, 2009.
[20] D. Crockford. *JavaScript: The Good Parts*. O'Reilly Media, Inc., 2008.
[21] K. R. Fall 和 W. R. Stevens. *TCP/IP illustrated, volume 1: The protocols*. addison-Wesley, 2011.
[22] E. Gamma, R. Helm, R. Johnson, R. E. Johnson, J. Vlissides 等. *Design patterns: elements of reusable object-oriented software*. Pearson Deutschland GmbH, 1995.
[23] H. Garcia-Molina. *Database systems: the complete book*. Pearson Education India, 2008.
[24] I. Gvero. Core java volume i: Fundamentals, by cay s. horstmann 和 gary cornell. *ACM SIGSOFT Software Engineering Notes*, 38(3):33–33, 2013.
[25] R. Harper. *Practical foundations for programming languages*. Cambridge University Press, 2016.
[26] S. Harris 和 D. Harris. *Digital design and computer architecture: Arm edition*. 2015.
[27] S. L. Harris 和 D. Harris. *Digital design and computer architecture*. Morgan Kaufmann, 2015.
[28] S. L. Harris 和 D. Harris. *Digital Design and Computer Architecture, RISC-V Edition*. Morgan Kaufmann, 2021.
[29] J. L. Hennessy 和 D. A. Patterson. Computer architecture: a quantitative approach. 2018.
[30] S. Hyde. *Write Great Code, Volume 3: Engineering Software*. No Starch Press, 2020.
[31] M. Kleppmann. *Designing data-intensive applications: The big ideas behind reliable, scalable, and maintainable systems*. O'Reilly Media, Inc., 2017.
[32] J. Kurose, K. Ross 和 J. Addison-Wesley. Computer networking: A top down approach.
[33] J. Levine. Linkers and loaders., 1999.
[34] J. R. Levine, J. Mason, J. R. Levine, T. Mason, D. Brown 和 P. Levine. *Lex & yacc*. O'Reilly Media, Inc., 1992.
[35] S. Meyers. *Effective STL: 50 specific ways to improve your use of the standard template library*. Pearson Education, 2001.
[36] S. Meyers. *Effective C++: 50 specific ways to improve your programs and designs*. Pearson Education, 2005.
[37] S. Meyers. *Effective modern C++: 42 specific ways to improve your use of C++ 11 and C++ 14*. O'Reilly Media, Inc., 2014.
[38] J. C. Mitchell. *Foundations for programming languages, volume 1*. MIT press Cambridge, 1996.
[39] S. Muchnick 等. *Advanced compiler design implementation*. Morgan kaufmann, 1997.
[40] C. Okasaki. *Purely functional data structures*. Cambridge University Press, 1999.
[41] J. K. Ousterhout. *A philosophy of software design, volume 98*. Yaknyam Press Palo Alto, 2018.
[42] D. Patterson 和 A. Waterman. *The RISC-V Reader: an open architecture atlas*. Strawberry Canyon, 2017.
[43] D. A. Patterson 和 J. L. Hennessy. Computer organization and design risc-v edition: The hardware software interface (the morgan kaufmann).
[44] D. A. Patterson 和 J. L. Hennessy. *Computer organization and design: The hardware/software interface*. 2013.
[45] D. A. Patterson 和 J. L. Hennessy. *Computer organization and design ARM edition: the hardware software interface*. Morgan kaufmann, 2016.
[46] J. L. Peterson 和 A. Silberschatz. *Operating system concepts*. Addison-Wesley Longman Publishing Co., Inc., 1985.
[47] B. C. Pierce. *Types and programming languages*. MIT press, 2002.
[48] B. C. Pierce. *Advanced topics in types and programming languages*. MIT press, 2004.
[49] W. Richard. *Unix network programming, volume 2: Interprocess communications*. 1999.
[50] D. M. Ritchie, B. W. Kernighan 和 M. E. Lesk. *The C programming language*. Prentice Hall Englewood Cliffs, 1988.
[51] L. Robert. *Linux kernel development*. Pearson Education India, 2018.
[52] A. Rubini 和 J. Corbet. *Linux device drivers*. O'Reilly Media, Inc., 2001.
[53] J. Sanders 和 E. Kandrot. *CUDA by example: an introduction to general-purpose GPU programming*. Addison-Wesley Professional, 2010.
[54] A. Silberschatz, H. F. Korth, S. Sudarshan 等. *Database system concepts, volume 5*.
[55] M. Sipser. Introduction to the theory of computation. *ACM Sigact News*, 27(1):27–29, 1996.
[56] W. R. Stevens, B. Fenner, A. M. Rudoff. *UNIX Network Programming Volume 1*. SMIT-SMU, 2018.
[57] W. R. Stevens, S. A. Rago 和 D. M. Ritchie. *Advanced programming in the unix environment, volume 4*. Addison-Wesley New York, 1992.
[58] W. R. Stevens 和 G. R. Wright. *TCP/IP Illustrated: volume 2*. Addison-wesley, 1996.
[59] W. R. Stevens 和 G. R. Wright. *TCP for transactions, HTTP, NNTP, and the UNIX domain protocols*. Addison-Wesley, 2000.
[60] B. Stroustrup. The c++ programming language (hardcover), 2013.
[61] A. B. Tanmor. Core java® volume ii: advanced features by cay s. horstmann 和 gary cornell. *ACM SIGSOFT Software Engineering Notes*, 39(3):24–25, 2014.
[62] R.-G. Urma, M. Fusco 和 A. Mycroft. *Java 8 in action*. Manning publications, 2014.

---

## 附录 A 关键编程范式（Key Programming Paradigms）

（提示：更多资源见 Wikipedia。）

### A.1 串行（Serial）

#### A.1.1 非结构化（Non-structured）

例如机器语言、汇编语言、早期带 goto 的高级语言。

#### A.1.2 结构化（Structured）

1. 命令式（图灵语言）
   (a) 过程式（Procedural）
   (b) 面向对象（Object-oriented）
2. 声明式（Declarative）
   (a) 函数式（Church 语言）
     （发展：无类型 → 有类型）
     i. 非纯（Impure）
     ii. 纯（Pure）
   (b) 逻辑（Church 语言）
   (c) 数据库（Databases）

多范式语言越来越流行。

### A.2 并行（Parallel）

#### A.2.1 数据并行（Data Parallel）

1. 高层：向量化
2. 低层：SIMT
3. 同步机制：barrier

#### A.2.2 任务并行（Task Parallel）

1. 并发机制
   (a) 高层：async/await（又称 future monad）
   (b) 低层：
     i. 多处理（multiprocessing）
     ii. 多线程（multithreading）
     iii. 协程（coroutines）
       A. stackful
       B. stackless
     iv. future、promise 等
     v. 回调（callbacks）
     vi. reactive extensions
2. 同步机制
   (a) 共享内存
   (b) 消息传递
   (c) 无锁编程（如使用原子操作）

#### A.2.3 分布式计算（Distributed Computing）

1. Map-Reduce
2. Transforms-Actions（Spark）

## 附录 B 有趣有用的库与工具清单

### B.1 Protocol Buffer 与 gRPC

- ProtoBuf：<https://protobuf.dev/>
- gRPC：<https://grpc.io/>

### B.2 Google Test 与 Google Mock

<https://google.github.io/googletest/>

### B.3 OpenTelemetry

<https://opentelemetry.io/>

一些像 DataDog 这样的可观测工具真的很好，但不是免费的。像 Jaeger 这样的免费工具也是好的替代。

### B.4 AWS SDK

### B.5 JAX

<https://jax.readthedocs.io/en/latest/>
