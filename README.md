# 华中科技大学 数据结构课程实验报告

## 基本信息

| 项目 | 内容 |
|------|------|
| **课程名称** | 数据结构 |
| **实验题目** | 线性表综合管理系统 & 基于邻接表的图演示系统 |
| **作者** | 徐靖杰 |
| **学号** | U202514843 |
| **学院** | 计算机科学与技术学院 |
| **班级** | 计算机类 2505 |
| **指导教师** | 孙伟平 |
| **完成日期** | 2026 年 6 月 15 日 |

## 实验内容

本报告包含两个独立的数据结构综合实验：

### 实验二：线性表综合管理系统

基于**单链表**的完整管理系统，涵盖两层操作模式：

- **单表模式**（18 项基本操作）：初始化、销毁、清空、判空、求长度、按位取值、按值查找、前驱后继、插入、删除、遍历、逆置、删除倒数第 N 个节点、冒泡排序、文件读写
- **多表模式**：支持按名称创建、选择、删除命名线性表（容量上限 10 个）

核心数据结构采用三层模型：`LNode`（节点）→ `NamedList`（命名链表）→ `LISTS`（集合容器）。

### 实验四：基于邻接表的图演示系统

基于**邻接表**的图操作与可视化演示系统：

- **单图模式**（18 项操作）：建图/销毁、顶点/边增删改查、DFS 与 BFS 遍历
- **多图管理模式**：支持创建、切换、删除命名图
- **BFS 应用**：最短路径长度计算、连通分量计数、顶点距离 < K 筛选
- **文件持久化**：图的保存与加载

核心数据结构：四层嵌套结构体——`VertexType` → `ArcNode` → `VNode` → `ALGraph`。

## 目录结构

```
.
├── Experimental_Report.tex       # 主 LaTeX 源文件
├── Experimental_Report.cls       # 文档类（HUST 实验报告样式）
├── Experimental_Report.cfg       # 文档类配置文件
├── Experimental_Report.bib       # BibTeX 参考文献库
├── Experimental_Report.bst       # 参考文献格式
├── Makefile                      # Linux/macOS 编译脚本
├── makethesis                    # Linux 编译入口
├── makethesis.bat                # Windows 编译入口
├── .gitignore                    # Git 忽略规则
├── images/                       # 图片资源（流程图、截图、示意图）
├── HUSTBlack.eps                 # 校徽矢量图（黑色）
└── HUSTGreen.eps                 # 校徽矢量图（绿色）
```

## 编译方法

本报告使用 **XeLaTeX** 编译，需要安装 TeX Live / MiKTeX 发行版。

### 依赖宏包

```
xeCJK, algorithm, algpseudocode, amsmath, amsthm, amssymb,
framed, mathtools, subcaption, xltxtra, bm, tikz, pgfplots,
titlesec, listings, xcolor, fontspec, microtype, enumitem, markdown
```

### Windows

```batch
makethesis.bat
```

### Linux / macOS

```bash
make
# 或
./makethesis
```

### 手动编译

```bash
xelatex -interaction=errorstopmode Experimental_Report.tex
bibtex Experimental_Report
xelatex -interaction=errorstopmode Experimental_Report.tex
xelatex -interaction=errorstopmode Experimental_Report.tex   # 两次以生成目录
```

## 排版亮点

- 代码块使用自定义 `elegantstyle`，支持语法高亮与行号
- 流程图采用 **TikZ/PGF** 原生绘制，风格统一
- 算法复杂度分析、数学推导使用 `mathderivation` 环境排版
- 图表索引与交叉引用自动编号

## 参考资料

本报告参考了如下内容：

- 严蔚敏，吴伟民. 数据结构（C 语言版）[M]. 北京：清华大学出版社
- [美] Kenneth H. Rosen 著；徐六通，杨娟，吴斌 译. 离散数学及其应用[M]. 北京：机械工业出版社，2019
- HUST 学位论文 LaTeX 模板（提供的 `Experimental_Report.cls` 文档类）

## 许可

本报告仅供课程学习与参考。如需引用，请注明出处。
