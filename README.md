# OscilloscopePlayer

本项目利用声卡作为数模转换，用于示波器X-Y模式下绘制线条，以实现播放视频。

## 原理

原始视频 -> FFmpeg解码 -> 边缘检测 -> 路径计算 -> 编码线条路径为音频 -> 通过声卡（充当廉价的DAC） 输出 -> 示波器X-Y模式输入分别连接左右声道 -> 播放

## 效果预览

https://youtu.be/VOMl51j2kIk

## 现状

目前未完成状态，勉强可以使用，供大家交流研究。

### 以下为将要实现的部分:

播放时候同时有原视频的声音输出(在有闲置声道或多声卡的设备上可用)

时间码显示

进度条拖拽

路径的计算相关算法需要进一步优化，尽量减少"拔丝"效果
