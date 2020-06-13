---
layout: post
title:  "乱序（ 0 1 2 9 44 265 …… ）"
categories: baidu-hi
tags: thinking
author: LZN
---

* content
{:toc}
'''
【引子】  

         最近数学课讲计数原理，老师出了这样一道题：3顶在外观上分辨不出的帽子分别属于甲乙丙，现在

3人随手拿起帽子戴上，问每个人都拿不到自己的帽子共有多少种情况。

    

        答案是两种，通过列举法可以轻易得到。随后，数学老师将情况扩展到自然数，给出了一组数列：0 1

2 9 44 265，并要求将前五组背下。现回家查阅相关信息，整理如下。

【正文】            

        0, 1, 2, 9, 44, 265, 1854, 14833, 133496, 1334961, 14684570, 176214841, 2290792932,……

        它们是n个元素可能出现的乱序情况数。

        在组合数学，乱序是指没有元素出现在自己原本位置的排列。通过容斥原理，我们可以证明，如果A

含有n个元素，则乱序排列的数目为[n! / e]，其中[x]表示最接近x的整数。

这也称为n的子阶乘，记为!n。可以推出，如果所有的双射都有相同的概率，则当n增大时，一个随机双射

是乱序排列的概率迅速趋近于1/e。

【参考文献】

http://zh.wikipedia.org/zh-cn/%E4%BA%82%E5%BA%8F 维基百科《乱序》

'''