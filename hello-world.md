# Hello World

## 1. 编写你的第一个shell程序

新建文件 `hello.sh`, 输入如下内容：

```
#!/bin/bash
echo "Hello World!"
```

如何运行这个脚本呢？有两个办法：

* 使用 `bash` 命令来运行，把 `hello.sh` 作为参数传给 bash 命令。在命令行中输入：

*（注：$ 不用输入，后面的命令行示例都已 $ 开头）*
> 命令 `bash` 接收的第一个参数就是 Bash 脚本的文件名，这是用的是 [相对路径](https://zh.wikipedia.org/wiki/%E8%B7%AF%E5%BE%84_%28%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%A7%91%E5%AD%A6%29#%E7%BB%9D%E5%AF%B9%E4%B8%8E%E7%9B%B8%E5%AF%B9%E8%B7%AF%E5%BE%84)。

```sh
$ bash hello.sh
Hello World!
```

* 修改 `hello.sh` 文件权限为可执行文件，然后直接执行脚本。在命令行中输入：

```sh
$ chmod +x hello.sh
$ ./hello.sh
Hello World!
```

## 2. Shell 脚本包含什么？

首先看第一行 `#!/bin/bash`， `#!` 是 Unix 系统对可执行脚本的约定标记，用于
告诉系统这个脚本需要什么解释器来执行，即使用哪一种 Shell。这里使用的是绝对路径 `/bin/bash`，一般 `bash` 被安装在 `/bin/bash`。比如 Python 脚本的第一行一般是 `#!/usr/bin/python`。

然后接着看第二行 `echo "Hello World!"`，其中 `echo` 就是调用的系统中的 `echo` 命令，这行代码跟在命令行中直接运行是一样的效果的。`echo` 命令就相当于其他编程语言的 `print` 函数，用于输出一行字符串到终端。

上面的脚本就包含了一行代码而已，一般完整的 Shell 脚本包含了这些：

- shell 关键字，比如：`if..then..else..fi` , `do..while..done`
- shell 命令，比如：`pwd`, `echo`, `grep`, `awk`, `sed`
- 函数 function, 一些复杂且重复的流程适合用函数来封装起来
- 流程控制，比如：`if..then` 或者 循环 `for..do..done`

