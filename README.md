# 易语言支持库开发包（易语言SDK）

## 说明

本仓库为一个易语言代码仓库，提供了针对易语言5.11及以前版本支持库的完整易语言开发SDK、静态库转换工具、静态库代码生成工具等。

过去了很久了，有时候还是会有人加我寻求这些工具+代码，所以开个仓库。欢迎有需要拿去使用或修改。

代码最后更新时间为2017.01.28，时隔4年未作出改动。

估计后面也不会改动，即便会做新的，也该也不会基于这个做的，看情况吧。

而且现在不清楚易语言的发展，很久没关注了。

**此外，本仓库使用了一些来自外部的工具，并且已提供了编译后的可执行文件在仓库中，并不保证能够安全使用（所有文件均来自4年前）。**

## 目录结构

- [SDK](./SDK)
  
  易语言支持库开发模块。提供了易语言支持库开发所需代码的基本封装，帮助您快速借助此模块快速在易语言上为易语言开发支持库（。。套娃，总觉得很绕口）。

  当时开发本SDK时我所使用的易语言为5.11版本，所以部分新加入的支持库功能未纳入本SDK中（比如授权）。但是已有功能不会被影响。

- [Demo](./Demo)

  提供了一个简易的易语言支持库的实现。包含以下功能：

  - 自定义附加功能（会出现在易语言的菜单里）。
  - 输出调试信息
  - 函数添加演示
  - 类添加演示
  - 组件添加演示
  - ...

- [Docs](./Docs)

  内含了来自易语言安装目录内的支持库开发文档。

- [Tools](./Tools)

  包含了与支持库相关的工具。

  - [静态库转换工具](./Tools/SalHeELibTools)
    
    因为易语言无法直接将动态链接库编译为lib文件，所以需要先编译为普通的DLL文件，然后借助此工具转换为易语言支持库的静态库，供静态编译。

    本工具中引用了外部工具，如Dll2Lib3.exe等，这些工具可以自行上网百度，或使用本仓库中提供的工具（但不一定保证安全性，所有的可执行文件均来自4年前）。

  - [静态库代码生成工具](./Tools/SalHeEStaticLibECodeMaker)

    有的支持库可能不存在静态库文件(lib)，使得使用其的源码无法被静态编译为目标程序。可以借助此工具为其生成其对应的静态库易语言代码并生成相应的静态库文件（将其包装后编译DLL，再使用[静态库转换工具](./Tools/SalHeELibTools)转换为lib文件）。


## 联系方式

- [SalHe](mailto:SalHe@qq.com)

## Thanks

- [Ex DirectUI](https://github.com/ikoude/ExDirectUI4.1)。使用易语言开的DirectUI库，最新版支持提供DLL给其他编程语言使用。

- [易语言](http://www.dywt.com.cn/)。尽管如今已很少使用易语言，但我还是很感谢易语言能在我初学编程时提供给我的中文编程环境，让我收获了不少的知识。

- [精易论坛](http://bbs.125.la)。感谢精易论坛为易友们提供的易语言编程交流的地方，也是我以往爱去的地方。