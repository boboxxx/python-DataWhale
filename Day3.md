**练习题**：

1、猜数字游戏

题目描述:

电脑产生一个零到100之间的随机数字，然后让用户来猜，如果用户猜的数字比这个数字大，提示太大，否则提示太小，当用户正好猜中电脑会提示，"恭喜你猜到了这个数是......"。在用户每次猜测之前程序会输出用户是第几次猜测，如果用户输入的根本不是一个数字，程序会告诉用户"输入无效"。

(尝试使用try catch异常处理结构对输入情况进行处理)

获取随机数采用random模块。

![](https://img-blog.csdnimg.cn/20200714230819193.png)

```python
# your code here
import random 
x = random.randint(1,100)


for i in range(1,101):
        print("第%d次猜,请输入一个整型数字："%i,end="")
        try:
            a = int(input(""))
        except TypeError as error:
            print('这不是一个整数，请输入一个整数。')
        if(a<x):
            print("太小")
        elif(a>x):
            print("太大")
        else:
            print("恭喜你猜到了这个数字是%d"%x)
            break
