# Shell教程笔记

Ref：Runoob.com

https://www.runoob.com/linux/linux-shell.html

Shell脚本的第一行一般会指定解释该脚本的Shell程序：

**#!** 告诉系统其后路径所指定的程序即是解释此脚本文件的 Shell 程序。

```shell
# 这是注释
#!/bin/bash
echo "Hello World !"
```

如何运行Shell脚本：

1. ##### 作为可执行程序

```shell
chmod +x ./test/sh #使脚本具有执行权限
./test/sh #执行脚本
```

**注意：** 这种方式需要脚本在第一行指定解释器。

2. ##### 作为解释器参数

将代码保存至文件中（后缀名不重要，但一般是.sh结尾），然后运行解释器

```shell
/bin/sh test.sh
/bin/php test.php #用php解释器运行脚本
```

## 1. Shell 变量

- ##### 变量的命名

- ##### 变量的定义

```shell
your_name='runoob.com'
```

**注意：**定义变量时等号**中间不能加空格**

- ##### 变量的使用

使用变量前需定义，只需在变量名前加上一个美元符号（``$``）

```shell
your_name = 'xdz'
echo $your_name
echo ${your_name} #{}只是为了识别变量的边界。加不加都行
```

- ##### 变量的重新赋值

变量重新赋值不需要加上$, 直接赋值就好

- ##### 只读变量

```shell
readonly your_name
# 变量设为只读后，不可被修改，不可被unset
```

- ##### 删除变量

```shell
unset your_name
```

变量被删除后不可被再次使用，unset也不可删除只读变量。

- ##### 变量的类型

|   局部变量    |
| :-----------: |
| **环境变量**  |
| **shell变量** |

- ##### Shell字符串

字符串可以用单引号，也可以用双引号，甚至可以不用引号

**单引号：**单引号里的字符会原样输出，即不可使用变量，也不能出现单独一个引号，无法打印单引号

**双引号：**双引号内可以有变量，也可以出现转义字符（转义双引号）

引号可以用来拼接字符串

- 获取字符串长度

```shell
echo ${#str} #获取字符串str的长度
```

- 提取子字符串

```shell
string='abcdefg'
echo ${string:1:3} #从下表为1的处截取长度为3的子串，输出bcd
```

- 查找子字符串

```shell
```

