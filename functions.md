## python内置函数
+ map()-根据提供的函数对指定的序列做映射。

      语法：manp(function,iterabl,...)
      返回值：pyton2.X返回列表；pyton3.X返回迭代器。

示例：
```python3
print list(map(lambda x: x **2,[1,3,5,7])) 
# 第一个参数function以参数序列的每一个元素调用function，返回包含每次function返回值的新列表。
# 运行结果为 [1,9,25,49]
```

+ enumerate()-用于将一个可遍历的对象，如列表、元祖或字符串组合为一个索引序列,同时列出数据和数据下标。

      语法：enumerate(sequence,[start=0])
      返回值：返回enumerate对象

示例：
```python3
name = ['lucy','lily','julia']
print list(enumerate(name))  #sequence为序列、可迭代对象；默认起始下标为0

seq = [(0, 'lucy'), (1, 'lily'), (2, 'julia')]
# 使用enumerate()的for循环：
for i, element in enumerate(seq):
    print(i, element)
# 运行结果为：
0 (0, 'lucy')
1 (1, 'lily')
2 (2, 'julia')
```

+ dict() -用于创建一个字典

      语法：class dict(**kwarg)
           class dict(mapping, **kwarg)  # mapping -- 元素的容器
           class dict(iterable, **kwarg)   # iterable -- 可迭代对象
      返回值：一个字典

示例：
```
dic = dict()
dic1 = dict(a='1', b=2, c=('test', 1))    # 传入关键字
dic2 = dict(zip(['one', 'two', 3], [1, 2, 'three']))   # 映射函数方式来构造字典
dic3 = dict([(0, 'false'), (1, 'true'), (3, 'none')])  # 可迭代对象方式来构造字典

print(dic)
print(dic1)
print(dic2)
print(dic3)

# 输出结果：
{}
{'a': '1', 'b': 2, 'c': ('test', 1)}
{'one': 1, 'two': 2, 3: 'three'}
{0: 'false', 1: 'true', 3: 'none'}
```
      
## python方法
+ split()-指定分隔符对字符串进行切片。

      语法：split(分隔符，num)  # 默认按照空格切分，切分次数为空格个数
      返回值：返回分割后的字符串列表。

示例：
```python3
str1 = 'I think everyday is worth celebrating.'
print(str1.split())
# 运行结果为 ['I', 'think', 'everyday', 'is', 'worth', 'celebrating.']
```
