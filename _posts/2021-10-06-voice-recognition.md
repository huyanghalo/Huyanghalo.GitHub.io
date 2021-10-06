---
layout: post
read_time: true
show_date: true
title: "调用讯飞语音api进行语音识别"
date: 2021-10-06
img: posts/20210420/post8-rembrandt.jpg
tags: [copyright, speech recognition, machine learning, artificial intelligence]
category: opinion
author: HU YANG
description: "how can we transfer audio to words?"
---
### AIM

this is us.mp3  TO  this.is us 字幕



### PROCEDURE

1. 讯飞官网   --- 语音转换 --- apiid 以及  key.详情点击[这里](https://www.xfyun.cn/)  

2. 相关接口代码--- 加入音频 --- 赋值给result 

3. 结果处理



### ATTENTION

1. 单独复制结果，保存为 [{},{},{},{}]的形式

~~~python
p9=[{"bg":"0","ed":"3800","onebest":"嗯","speaker":"0"}]
~~~

3. with 语句 写入 result.txt

```python
with open("result.txt","w") as f:
	for i in list(i for i in p9):
		f.write(i["onebest"]+"\n\n")
```

