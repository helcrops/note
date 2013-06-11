The Julia Manual
1. Introduction
1. Getting Started
1. Variables
1. Integers and Floating-Point Numbers
1. Mathematical Operations and Elementary Functions
1. Complex and Rational Numbers
1. Strings
1. Functions
1. Control Flow
1. Scope of Variables
1. Types
1. Methods
1. Constructors
1. Conversion and Promotion
1. Modules
1. Metaprogramming
1. Multi-dimensional Arrays
1. Linear algebra
1. Parallel Computing
1. Running External Programs
1. Calling C and Fortran Code
1. Julia Packages
1. Performance Tips
##开始：

最简单的方法是用一个交互界面：终端输入 
    $julia
退出交互系统 C-D 或者输入 quit()类似python
变量ans代表最后一个表达式的值。

运行脚本 
    $julia file.jl arg1 arg2

例如：建立一个文件，输入
    for x in AGRS; println(x); end
保存为 args.jl
终端输入:
    julia args.jl aaa bbb
结果：
    aaa
    bbb
或者终端运行：
    julia -e 'for x in ARGS; println(x); end' aaa bbb
结果相同

Julia命令行参数：
julia [选项] [程序] [参数]
    -v --version 显示版本
    -q --quiet 不显示欢迎词
    -H --home=<dir> 载入属于<dir>目录的文件
    -T --tab=<size> 设置REPLtab宽度size
    -e --eval=<expr> 运行表达式<expr>
    -E --print=<expr> 运行并显示表达式
    -P --post-boot=<expr> boot后运行<expr>
     -L --load=file boot后载入file
     -J --sysimage=file 随着给定的系统文件启动
     -p n 运行n个进程
     --machinefile file       Run processes on hosts listed in file
     --no-history 不加载或记录历史(命令)
     -f --no-startup 不加载~/.juliarc.jl
     -F 加载~/.juliarc.jl后处理剩下的输入
     -h --help     显示帮助