# 图达通雷达相机的路侧感知后融合项目
如题，基本的思路很简单，使用自研硬件进行两个设备的结果级融合。其中激光雷达采用图达通300线雷达，使用点云目标检测器进行目标检测，例如pointpillars（openPCDet)。
图像目标检测器则采用yolo系列进行前向视角下的目标检测，例如yolov7。

## 激光雷达检测
为了解决标注困难的问题，有百度-清华合作的DAIR-V2X数据集作为参考，其已经标注了大量的雷达bounding box。训练时采用该数据则可。

## 图像检测
目前图像方面的检测器泛化性好，采用公开发布的预训练yolov7权重，即可得到一个还可以的效果。
