# -人脸信息处理-
1.预处理（注意保留边缘信息）（图像大小限定、光线增强、减少噪声）
1.1光照补偿
1、差值补偿
2、讲图像所有像素亮度（非线性校正后）从高到低排。取前5%的像素，若数目足够多，讲它们的亮度做“参考白”（RGB均调至255）。整幅图像的其他像素点色彩值按这一调整尺度变换。（-1论文）

1.2滤波（去光照预处理）
1、中值滤波（图像非线性滤波，在一定程度上去除噪声，也可设计为消除方向性光照所引起的阴影）（-1论文）
中值滤波算法使用滑动窗口技术，把窗口中心对应的图像像素修改为窗口所覆盖的所有的像素的中间值(即把窗口覆盖的所有像素值按升序或降序顺序排列，然后取中问值)。这样一来，噪声就可以被去除，也较好的保留了边缘信息。
2、去光照预处理方法包括直方图均衡、图像非线性滤波、Gabor滤波、灰度微分和对数变换等
直方图均衡：改变图像的灰度值，提高图像的对比度。好处：1部分减小不同人脸图像的亮度差别；2使灰度值充分占据灰度值范围，提高图像对比度。
Gabor及其改进滤波器：（生理学研究）简单细胞的反应可以用二维Gabor近似，增强轮廓。
灰度微分：光照变化极大影响灰度图像，但较少影响其灰度微分图
对数变换：（生理学）视网膜细胞对输入图像的反应是非线性的，可用对数函数近似。

2、人脸定位（基于模板、基于统计学习、基于特征不变性）
2.1肤色特征
2.2头发特征
2.3人脸轮廓结构

3、轮廓提取
3.1双边滤波（保边去噪：两个函数：一个函数是由几何空间距离决定滤波器系数。另一个由像素差值决定滤波器系数）

当人脸被准确分割出来，提取人脸轮廓
五官！！！
