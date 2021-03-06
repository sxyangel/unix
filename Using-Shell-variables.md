# Shell 变量 #

变量就是被赋值后的字符串。那个赋给变量的值可以是数字、文本、文件名、设备或其他类型的数据。  

本质上，变量就是执行实际数据的指针。shell 可以创建、赋值和删除变量。  

## 变量名 ##

变量名仅能包含字母、数字或者下划线。

约定俗成的，Unix shell 的变量名都使用大写。

下面是一些有效的变量名的例子：

    _ALI
    TOKEN_A
    VAR_1
    VAR_2



下面是一些无效的变量名的例子：

    2_VAR
    -VARIABLE
    VAR1-VAR2
    VAR_A!

不能使用！、*、-等字符的原因是，这些字符在 shell 中有特殊用途。

## 定义变量 ##

变量可以按照如下方式来定义：

    variable_name=variable_value

比如：

    NAME="Zara Ali"

上述例子定义了变量 NAME，然后赋值 "Zara Ali".这种类型的变量是常规变量，这种变量一次只能赋值一个。

shell 可以随心所欲的赋值。比如：

    VAR1="Zara Ali"
    VAR2=100

## 访问变量 ##

为了获取存储在变量内的值，需要在变量名前加 $.

比如，下面的脚本可以访问变量 NAME 中的值，然后将之打印到 STDOUT:

    #!/bin/sh
    
    NAME="Zara Ali"
    echo $NAME

会出现下面的值：

    Zara Ali

## 只读变量 ##

shell 使用只读命令提供了使变量只读化的功能。这样的变量，都不能被改变。

比如，下面的脚本中，对变量 NAME 的值进行修改，系统会报错：

    #!/bin/sh
    
    NAME="Zara Ali"
    readonly NAME
    NAME="Qadiri"

会出现如下结果：

    /bin/sh: NAME: This variable is read only.

## 删除变量 ##

变量的删除会告诉 shell 从变量列表中删除变量从而，无法对其进行跟踪。一旦用户删除了一个变量,将无法访问存储在变量中。

下面是使用 **unset** 指令的例子：

    unset variable_name

上述指令会取消已定义变量。下面是简单的例子：

    #!/bin/sh
    
    NAME="Zara Ali"
    unset NAME
    echo $NAME

上述例子不会显示任何信息，不用使用 **unset** 来取消 只读的变量。

## 变量类型： ##

shell 脚本被执行的时候，来回存在如下三种变量类型：

1. **局部变量**：该类型变量只会在当前 shell 实例内有效。他们无法适用于由 shell 启动的程序。他们仅在命令提示符处进行设置。
1. **环境变量：**环境变量对 shell 的任何子进程都有效。部分程序是需要正确的调用函数才需要环境变量。通常，shell 脚本只会定义程序运行需要的环境变量。
1. **Shell 变量：**该类型变量是由 shell 设置的专用变量，是用来正确调用函数用的。有时这些变量是环境变量，有时是局部变量。

