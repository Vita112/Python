
## shell编程

+ 创建shell脚本文件
  　　
使用文本编辑器将要执行的命令打包命名为 filename.sh，使用`chmod +x　文件名`赋予可执行权限，然后在终端输入`$ ./filename.sh`就可以运行这个脚本文件了。

    规范的脚本文件中还应该包含以`＃`开头的注释；文件第一行使用`#! /bin/bash`,指明脚本所需要的shell。
    
+ 在shell中使用函数
```
函数名（）
{
函数体
}
```
__调用函数时，直接写函数名，而不需要写小括号__

+ 在shell中使用变量

> 使用变量时，要在变量前加上`$`符号，示例：
```
#! ./bin/bash
player1=YOGA
player2=KEN
today=`date %Y%m%d` #将命令的运行结果赋值给变量
echo $player1
echo"Game Start!${player1}vs${player2}" #使用{}表明变量
echo $today
```
输出结果为：<br>

    YOGA
    Game start!YOGA vs KEN
    当前日期
> `exprt`命令对字符串变量进行数学计算，示例：<br>
```
#! ./bin/bash
num=4
num=`exprt $num + 1`
echo $num
```
__环境变量__
用户变量：用户自己定义的变量<br>
环境变量：类似于C中的全局变量，在`整个系统`中都有效，一旦设定，在整个系统中任何时候、任何地方进行访问。示例：
```
exprt env_num=8
echo $env_num
```
> 使用&修改环境变量，共享脚本

    $TZ 获取本系统所在时区
    $HOME 获取当前用户的家目录地址

特殊变量<br>
    
    $n：执行本脚本所加的第n个参数，n=0~9，其中n=0时，代表脚本本身的名称。
    $*：执行本脚本所加的所有参数，不包括脚本名本身
    $#：执行本脚本所加的参数个数
    $$：代表本脚本的PID
  
+ shell中的条件判断
`if`条件判断
```
kill()
{
    if [ "$1" = "me" ]; then
    # 一定要注意空格，空格错误，则脚本错误；
    # if的工作是：根据后面命令的返回值，判断程序走哪条分支。例如：if ls -l /home; then，当`ls -l /home`这条命令执行成功，返回真值，就执行后面的语句。
        echo "You are dead..."
    else
        echo "$1 is dead..."
    fi
}
```

    `[ "$1" = "me" ]`是一条命令：
    `[`是命令名，判断后面参数所组成的表达式的值是真还是假，并返回，要求最后一个参数必须为]。"$1",=,"me",]都是参数，参数间必须要有空格。

常用判断参数<br>
文件检查，算数比较运算，字符串运算<br>
`case`语句实现多分支判断
```
#! /bin/bash
echo "input a number: "
read num
case $num in
one) echo "我认识，这是一";; #双分号表示本条case结束
two) echo "我认识，这是二";;
three) echo "这个我得想想......"
    echo "啊，我想起来了，这是三！";;
*) echo "这个我真的不认识了。。。";; #*)表示其他数值
esac #表示结束
```
    
    

    
    
