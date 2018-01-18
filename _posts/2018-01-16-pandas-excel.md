---
layout: post
title:  "利用pandas生成excel文件"
categories: python
tags:  pandas excel 
author: LZN
---

* content
{:toc}
需要将几个pandas生成的csv文件合并到excel的不同sheets里，手动是一件比较蛋疼的工作，查了下python对excel的支持，发现pandas天生支持这类操作，大喜过望。测试之。
pandas写出xls简直像csv一样简单，而且是内生支持，不需要安装任何其他库。

以应用情景为例，写入不同的sheets，具体如下：

``` python
# open a new xlsx writer
writer1 = pd.ExcelWriter(out_dir+get_outfile_name(sta_num, 'Daily'))
for pos, spe in enumerate(species):
    # parser data
    pt=pd.read_csv(in_dir+get_file_name(sta_num, corr_algthm, spe, 'Daily'), parse_dates=True, skiprows=1, names=['time', '10H', '12H', '14H', '16H', 'max'], index_col='time')
    pt.to_excel(writer1, spe)
# save xlsx
writer1.save()
```


**Updated 2018-01-16**