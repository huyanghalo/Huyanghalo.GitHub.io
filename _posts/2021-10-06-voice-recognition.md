---
layout: post
read_time: true
show_date: true
title: "调用讯飞语音api进行语音识别"
date: 2021-10-06
img: posts/20210420/post8-rembrandt.jpg
tags: [copyright, creativity, neural networks, machine learning, artificial intelligence]
category: opinion
author: HU YANG
description: "how can we transfer audio to words?"
---
# Aim

this is us.mp3  TO  this.is us 字幕

# Procedure

讯飞官网   --- 语音转换 --- apiid 以及  key.详情点击[这里](https://www.xfyun.cn/)  

相关接口代码--- 加入音频 --- 赋值给result 

结果处理

# Attention

单独复制结果，保存为 [{},{},{},{}]的形式

p9=[{"bg":"0","ed":"3800","onebest":"嗯","speaker":"0"}]

with 语句 写入 result.txt

with open("result.txt","w") as f:

    for i in list(i for i in p9):
    
        f.write(i["onebest"]+"\n\n")
 
