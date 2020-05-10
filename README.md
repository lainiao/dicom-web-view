
虽然GitHub注册的很早2010年就注册了，但是基本上没有用过，用的最多的大概是码云，有几十个项目，这次打算使用Github的原因有2个，是期望可以和大家一起完成这个项目。

# dicom-web-view
计划实现一个基于Web技术的Dicom 阅片系统。 初步打算实现基本的Dcm 文件展示，调窗，旋转，缩放，标记 ，基本测量等功能。该系统计划同时同时支持PC和Mobile。
项目计划使用Springboot 最后作为后端，Mysql作为数据库，MINIO 作为线下使用的存储中间件，Ali OSS 作为线上支持的存储中间件，前端阅片插件目前计划使用cornerstone.js

cornerstone.js ，使用这个插件是因为目前这个算是开源里面相对比较成熟的插件，但是不排除后期自己写，因为我对在前端阅片使用原始的DCM文件进行阅片其实并不满意，最重要的因素是DCM文件较大，第二个因素是前端解析DCM文件其实是比较耗费计算资源。 如果这个项目完成以后，看看有没有时间，写一个实现，把DCM文件转成一种特殊的图片，在前端进行阅片。 只所以要转成一种特殊的图片的原因是因为，现有的DCM转图片，会将DCM文件转化成固定的窗宽窗位的图片，映射成只有256个灰度的图片，这样会丢失原始的图像信息，失去了阅片的意义。如果转成这种特殊的图片的话，就不会丢失像素信息，任然可以保持最高65536个灰度级的信息，不会丢失图像信息，当然这个以后在说，先实现功能，这个属于优化层面的功能。

因为自己平时工作比较忙，就慢慢更新这个项目，先把自己的思路放上来。
![image](http://raw.githubusercontent.com/lainiao/dicom-web-view/master/document/img/1.png)
数据库
![image](http://raw.githubusercontent.com/lainiao/dicom-web-view/master/document/img/2.png)
主要流程
![image](http://raw.githubusercontent.com/lainiao/dicom-web-view/master/document/img/3.png)
