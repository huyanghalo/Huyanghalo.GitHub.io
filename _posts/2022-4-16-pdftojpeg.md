---
layout: post
read_time: true
show_date: true
title: "pdf 转为jpeg或者png"
date: 2022-4-16
img: posts/machinel.jpg
tags: [Computer]
category: ml
author: HU YANG
description: "my babe" 
---

###  环境变量设置

### PDF2image 将PDF转为 jpeg或 png

#### 配置环境

python +pdf2image +poppler(http://blog.alivate.com.au/poppler-windows/)，并将poppler 设置为环境变量



####  用法code

~~~python
from pdf2image import convert_from_path,convert_from_bytes

#方法一 直接是 英文路径，不能出现中文
images=convert_from_path(r"D:\desktop\a.pdf",dpi=96,output_folder=r"D:\desktop\pdfconvert",fmt="JPEG",output_file="ok",thread_count=4)

#方法二
images=convert_from_path(r"D:\desktop\a.pdf",dpi=96)
for image in images:
    image.save("D:/desktop/pdfconvert"+"/"+"cihui_%s.png"% images.index(image),"PNG")
#前者更方便些
~~~

#### 效果图

![map](./assets/img/posts/20220416/1.png)





参考链接：

1. https://blog.csdn.net/qq_28550263/article/details/115467193
2. https://blog.csdn.net/zbj18314469395/article/details/98329442
