# Shaweima Final Task

一个使用 C++ 和 EasyX 编写的大学数据结构课程设计。程序以图形界面管理用户/客户记录，提供查看、编辑、查询、排序等操作，并包含队列、向量和快速排序等数据结构练习代码。

## 功能概览

- 图形化主窗口、用户列表查看和编辑界面。
- 新增、删除、修改和查询记录，支持按姓名或编号查找。
- 按编号或积分排序，并通过表格分页浏览记录。
- 使用文本文件保存记录，仓库包含 `Persons.txt` 作为数据文件。
- 自定义 `Queue`、`Vector` 和 Quick Sort 示例，便于学习基础数据结构与模板。

## 技术栈

- C++（Visual Studio 工程，MSVC v143）
- Windows API
- EasyX 图形库

这是 Windows 桌面程序，不是跨平台命令行项目。仓库中的 Visual Studio 工程包含原开发机的绝对 include 路径；在其他电脑上打开前，请将其改为本机 EasyX 和项目文件的位置。

## 使用 Visual Studio 运行

1. 安装 Visual Studio 2022，并勾选“使用 C++ 的桌面开发”工作负载。
2. 安装 EasyX，并确认 EasyX 的头文件和库文件对当前目标平台（Win32 或 x64）可用。
3. 克隆仓库后打开 [`Shaweima.sln`](Shaweima.sln)。
4. 在项目属性中修正 EasyX/include 路径，选择 `Debug` 或 `Release` 以及 `Win32` 或 `x64`。
5. 构建并运行。程序通过 `main.cpp` 创建主窗口并进入消息循环。

项目数据文件和图片资源按相对路径读取。运行时请确保工作目录包含 `Persons.txt`、`background.jpg` 等资源；如果记录文件为空，程序会从空数据开始。

## 主要文件

| 文件 | 职责 |
|---|---|
| `main.cpp` | 创建主窗口并启动界面消息循环 |
| `Window.h/.cpp` | 主界面状态、功能按钮和页面切换 |
| `Widget.h/.cpp`、`Button.h/.cpp` | EasyX 基础控件 |
| `Table.h/.cpp` | 用户数据表格、分页、查询和编辑展示 |
| `Manager.h/.cpp` | 记录的加载、保存、增删改查和排序 |
| `Person.h` | 用户/客户记录结构 |
| `Queue.h/.cpp`、`Vector.h`、`Sort.h` | 课程设计中的数据结构和排序练习 |
| `Persons.txt` | 本地文本数据文件 |

## 数据与隐私

程序会在本地读写 `Persons.txt`。请先备份需要保留的数据；不要把真实个人信息提交到公开仓库。当前仓库附带的数据文件为空，适合作为初始数据文件。

该项目主要用于课程学习和代码参考。EasyX 与 Visual Studio 的安装、链接方式可能因版本和目标平台而不同，请按本机环境调整工程配置。


