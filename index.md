## Shell 教程
### 第一个shell脚本
```
#!/bin/bash
echo "Hello World !"
#! 是一个约定的标记，它告诉系统这个脚本需要什么解释器来执行，即使用哪一种 Shell。
echo 命令用于向窗口输出文本。
```
### 运行 Shell 脚本有两种方法：
1、作为可执行程序

将上面的代码保存为 test.sh，并 cd 到相应目录：
```
chmod +x ./test.sh  #使脚本具有执行权限
./test.sh  #执行脚本
```

### Shell 变量
```
your_name="runoob.com"
除了显式地直接赋值，还可以用语句给变量赋值，如：
for file in `ls /etc`
```

### 使用变量
```
#!/bin/bash
your_name="wangshaojun"
echo $your_name
echo ${your_name}
```

变量名外面的花括号是可选的，加不加都行，加花括号是为了帮助解释器识别变量的边界，比如下面这种情况：
```
#!/bin/bash
for skill in Ada Coffe Action Java; do
echo "I am good at ${skill}Script"
done
执行结果: 
I am good at AdaScript
I am good at CoffeScript
I am good at ActionScript
I am good at JavaScrip
```
推荐给所有变量加上花括号，这是个好的编程习惯。


已定义的变量，可以被重新定义，如：
```
#!/bin/bash
your_name="tom"
echo $your_name
your_name="alibaba"
echo $your_name
执行结果:
tom
alibaba
```
### 只读变量

只读变量的值不能被改变。
```
#!/bin/bash
myUrl="http://www.w3cschool.cc"
readonly myUrl
myUrl="http://www.runoob.com"
执行结果:./test5.sh: line 4: myUrl: readonly variable
```

### 删除变量

使用 unset 命令可以删除变量。语法：
```
unset variable_name
例子:
#!/bin/sh
myUrl="http://www.runoob.com"
unset myUrl
echo $myUrl
执行结果为空
```

### Shell 字符串
```
1. str='this is a string'
2.
#!/bin/sh
your_name='wsj'
str="Hello, I know your are \"$your_name\"! \n"
echo $str
运行结果:Hello, I know your are "wsj"! \n

3.拼接字符串
#!/bin/sh
your_name="wsj"
greeting="hello, "$your_name"!"
greeting_1="hello, ${your_name} !"
echo $greeting $greeting_1
运行结果:hello, wsj! hello, wsj !

4.获取字符串长度
#!/bin/sh
string='abcd'
echo ${#string}
运行结果：4

5.提取子字符串
#!/bin/sh
string="runoob is a great site"
echo ${string:1:4}
运行结果:4

6.
#!/bin/sh
string="runoob is a great company"
echo `expr index "$string" is`
运行结果:8
```
### Shell 数组
```
定义:数组名=(值1 值2 ... 值n)
#!/bin/sh
array_name=(value0,value1,value2,value3)
1.输出所有元素:
echo ${array_name[@]}
取得数组单个元素的长度：#!/bin/sh
array_name[0]=value0
array_name[1]=value1
array_name[2]=value3

2.数组长度:
length=${#array_name[@]}
echo $length
length=${#array_name[*]}
echo $length
第一个元素的长度
lengthn=${#array_name[0]}
echo $lengthn

3.获取元素第一个元素
#!/bin/sh
array_name=(1 2 3 4 5)
echo ${array_name[0]}
运行结果:1
```








