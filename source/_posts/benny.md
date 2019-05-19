---
title: benny
date: 2018-12-23 12:20:14
tags:
---

<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
  </script>
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>


# Markdown 基本语法
## 1.1 标题
Markdown中包含了6级的标题，每级标题的字号是不一样的，由1-6递减，分别为#，##，...,######. 一二级标题自带分格线
### 1.1.1 二级标题

## 1.2 段落与分隔线
### 1.2.1 段落
在Markdown中写作一个段落的方法很简单，我们使用一个空行来表示就好了

### 1.2.2 分隔线
___
___

## 1.3 粗体及斜体
\*\*文字\*\* 显示为粗体

\*文字\* 显示为斜体

**今天**是个*不一样*的_日子_

## 1.4 引用代码
程序员在blog中添加代码是最经常不过的了，可以通过如下的方式添加一段代码，也可以指定代码的种类。
使用首尾各三个\`\`\`。在开头的三个\`\`\`后可以添加语言名称

## 1.5 添加图片和链接
* 添加链接，使用两个中括号来表示，前一个中括号为链接说明，后一个中括号为链接地址。格式如下：[]\(\)

[计蒜客 30999](https://nanti.jisuanke.com/t/30999)

* 添加图片，在添加链接的的前一个中括号前添加一个!(当然是半角的)号。格式：！[]\(\)

[^_^]: ![](https://menci-oi.sengxian.com/images/avatar.png1)


[//]: # (<div align="left"><img width="65" height="75" src="https://menci-oi.sengxian.com/images/avatar.png"/></div>)


[//]: # (a)

[^_^]:  b

c

d
## 1.6 有序列表和无序列表
有序列表 数字\.空格   
无序列表 \* 空格
1. 工作
2. 学习
3. 生活


* 工作
* 学习
* 生活

## 1.7 任务列表
**购物清单**

- [ ] 一次性水杯
- [x] 西瓜
- [ ] 豆浆
- [x] 可口可乐
- [ ] 小茗同学

# Markdown 高级语法
## 2.1 表格
| Header1 | Header2                          |Header3
|:---------|:----------------------------------:|-------------------:
| item 1  | 1. one<br />2. two<br />3. three | 50
| item 2  | 4. four<br />5. five<br />6. six | 60

## 2.2 流程图
Github上的语法说明：[Markdown流程图说明](http://blog.csdn.net/whqet/article/details/44281463)

```flow
st=>start: Start
```

&emsp;&emsp;春天来了，又到了万物复苏的季节。



```cpp
#include <cstdio>
int main()
{
    return 0;
}
```

<img align="right" src="https://raw.githubusercontent.com/mzlogin/mzlogin.github.io/master/images/posts/markdown/demo.png"/>

这是一个示例图片。

图片显示在 N 段文字的右边。

N 与图片高度有关。

刷屏行。

刷屏行。

到这里应该不会受影响了，本行应该延伸到了图片的正下方，所以我要足够长才能确保不同的屏幕下都看到效果。

| Header1 | Header2                          |
|---------|----------------------------------|
| item 1  | 1. one<br />2. two<br />3. three |


$9 = 3 \times 3$ 

 bbb $ E = mc ^ 2$
  $$ A=a \bullet i+b \bullet j=[i,j] \bullet [a;b]=基\bullet坐标 \tag{3}$$
$$
E=mc^2
$$

$$
\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}
$$

