+ map()-根据提供的函数对指定的序列做映射。

语法：manp(function,iterabl,...)<br>
返回值：pyton2.X返回列表；pyton3.X返回迭代器。<br>

示例：<br>
```python3
>>> map(lambda x: x **2,[1,3,5,7]) 
# 第一个参数function以参数序列的每一个元素调用function，返回包含每次function返回值的新列表。
[1,9,25,49]
```
+ split()-指定分隔符对字符串进行切片。

语法：split(分隔符，num)  # 默认按照空格切分，切分次数为空格个数<br>
返回值：返回分割后的字符串列表。<br>

示例：<br>
```python3
str1 = 'I think everyday is worth celebrating.'
print str1.split()
['I','think','everyday','is','worth','celebrating.']
```

+ enumerate()-用于将一个可遍历的对象，如列表、元祖或字符串组合为一个索引序列,同时列出数据和数据下标。

语法：enumerate(sequence,[start=0])<br>
返回值：返回enumerate对象<br>

示例：<br>
```python3
>>> name = ['lucy','lily','julia']
>>> print enumerate(name)  #sequence为序列、可迭代对象；默认起始下标为0
>>> [(0,'lucy')],(1,'lily'),(2,'julia')]
# 使用enumerate()的for循环：
>>> for i,element in enumerate(seq):
        print i ,element
```
