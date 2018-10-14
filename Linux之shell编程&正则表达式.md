
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
## 调用函数时，直接写函数名，而不需要写小括号

+ 在shell中使用变量

> 使用变量时，要在变量前加上`$`符号，示例：
```
#! ./bin/bash
player1=YOGA
player2=KEN
echo $player1
echo"Game Start!${player1}vs${player2}"
```
输出结果为：<br>

    YOGA
    Game start!YOGA vs KEN
    
    
