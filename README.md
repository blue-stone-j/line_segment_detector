# line_segment_detector

### CannyLines

### EDlines

### FLD

### Hough_line

### lsd(line_segment_detector) algorithm
在线性时间（linear-time）内得到亚像素级准确度的直线段检测算法。
1. 以 s=0.8的尺度对输入图像进行高斯核采样。
2. 计算每一个点的梯度值以及梯度方向（level-line orientation）
3. 根据梯度值对所有点进行伪排序（pseudo-ordered）
4. 梯度阈值（小梯度值抑制）
5. 区域生长算法用于生成一个line support region。
6. 矩形估计：上一步形成line-support region的一系列相邻的离散点，需要将他们包含在一个矩形框内R，这个可以看做宽度为R的宽，长度为R的长的候选直线。R选择能包含line-support region的最小矩形，所有点的梯度规范化值平均计算重心，R长轴的方向设置为R的方向。矩形的主方向被设置为矩阵的最小特征值对应的特征向量的角度。
7. NFA（Number of False Alarms）计算：用来验证矩形是否可以作为检测线段，方法是基于 “a contrario approach and the Helmholtz principle ”. “the Helmholtz principle”：在完美噪声图像图像中不应该检测到目标；“a contrario approach”：一个不会检测到目标的噪声图像。



### LSM

### LSWMS

### MCMLSD
