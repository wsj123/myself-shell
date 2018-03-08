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
