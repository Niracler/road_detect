road\_detect
------------
道路识别

目录
----
-   [road\_detect](#road_detect)
-   [概述](#概述)
    -   [课程设计的目的](#课程设计的目的)
    -   [课程设计任务及要求](#课程设计任务及要求)
    -   [开发该系统软件环境及使用的技术说明](#开发该系统软件环境及使用的技术说明)
-   [系统设计的基本概念与原理](#系统设计的基本概念与原理)
    -   [系统基本工作流程](#系统基本工作流程)
    -   [车道线检测算法设计](#车道线检测算法设计)
    -   [道路标示牌检测算法设计](#道路标示牌检测算法设计)
    -   [用户接口设计](#用户接口设计)
-   [系统实施详细说明及结果](#系统实施详细说明及结果)
    -   [道路检测算法的实现](#道路检测算法的实现)
    -   [道路标示牌检测算法实现](#道路标示牌检测算法实现)
    -   [系统运行结果及算法性能](#系统运行结果及算法性能)
    -   [课程设计总结](#课程设计总结)
-   [参考文献](#参考文献)

重要文档链接
-----------
- [《机器视觉》课程设计说明](docs)

概述
----

### 课程设计的目的

### 课程设计任务及要求

> 描述本课程设计的主要任务及要求

### 开发该系统软件环境及使用的技术说明

描述系统开发时所使用的开发环境及涉及到的技术

系统设计的基本概念与原理
------------------------

> 应包含核心代码

### 系统基本工作流程

> 系统整个工作流程图及文字描述

### 车道线检测算法设计

> 算法流程图，文字描述

1. 对原视频进行反透视变换，将视角转变为鸟瞰图。

2. 对视频进行一些预处理，如腐蚀膨胀，平滑处理等，设置ROI，减少画面中车道线以外的干扰物的影响。

3. 进行Canny变换，检测出画面的边缘并且对图像自动进行二值化处理。

4. 所得图像进行Hough变换，通过阀值，线段最短长度，连接为线段的最长间隔的设定来检测出画面中存在的直线。

5. 直线筛选，计算第四步所得线段的斜率，从中挑选符合要求的线段，并用cvLine函数标示到画面中。

6. 将所得画面再次进行透视变换，变回原视角。


### 道路标示牌检测算法设计

> 算法流程图，文字描述

### 用户接口设计

> 接口设计思路，文字描述

系统实施详细说明及结果
----------------------

### 道路检测算法的实现

> 关键代码及文字说明

### 道路标示牌检测算法实现

> 关键代码及文字说明

### 系统运行结果及算法性能

> 给出算法处理的效率（每次处理所需要的时间）和算法的准确率的统计。

### 课程设计总结

> 简要描述设计过程中遇到的问题，解决的方式

参考文献
--------
- OpenCV官方参考文档  
- Github网站  
- https://github.com/tatsuyah/Lane-Lines-Detection-Python-OpenCV  
- https://github.com/naokishibuya/car-finding-lane-lines  
- https://github.com/georgesung/advanced_lane_detection  
- https://github.com/DavidAwad/Lane-Detection  
- http://www.transistor.io/revisiting-lane-detection-using-opencv.html  
- [基于opencv的车道线实施检测（浙江大学）](https://wenku.baidu.com/view/a93bb15384254b35eefd34bd.html)
- https://www.bilibili.com/video/av23653073/