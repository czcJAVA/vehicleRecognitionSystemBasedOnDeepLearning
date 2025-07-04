## 基于深度学习的车辆识别系统

## 项目功能分析

这是一个基于深度学习的车辆识别系统，主要功能包括：

1. **车牌识别**：
   - 检测图像中的车牌位置
   - 识别车牌号码
   - 识别车牌颜色（黑色、蓝色、绿色、白色、黄色等）
   - 支持单层和双层车牌识别
   - 识别危险品车牌

2. **车辆识别**：
   - 车辆颜色识别（黑色、蓝色、黄色、棕色、绿色、灰色、橙色、粉色、紫色、红色、白色）
   - 车型品牌识别

3. **多种输入方式**：
   - 支持图片输入
   - 支持视频文件输入
   - 支持摄像头实时输入

4. **友好的图形用户界面**：
   - 使用PyQt5开发的现代化界面
   - 支持图像放大查看
   - 支持处理进度显示
   - 结果可视化展示
    ## 技术栈

1. **编程语言**：
   - Python

2. **深度学习框架**：
   - PyTorch：用于模型加载和推理
   - ONNX Runtime：用于某些模型的推理加速

3. **计算机视觉库**：
   - OpenCV：图像处理、视频处理
   - Numpy：数学计算

4. **GUI框架**：
   - PyQt5：构建图形用户界面

5. **模型架构**：
   - YOLOv5：用于车辆和车牌检测
   - 自定义网络：用于车牌字符识别、车辆颜色识别等

6. **其他技术**：
   - 透视变换：用于车牌校正
   - 非极大值抑制(NMS)：用于过滤重复检测框
   - 图像预处理：缩放、归一化等

## 深度学习大模型运行效果展示（一：GUI可视化运行界面）
1.启动程序并加装模型成功
![contents](pictrue/picture1.png)
2.支持图片识别和摄像头识别以及视频视频
![contents](pictrue/picture2.png)
3.上传图片识别
![contents](pictrue/picture3.png)
![contents](pictrue/picture4.png)
![contents](pictrue/picture5.png)
4.支持细节展示（图片放大，详细查看）
![contents](pictrue/picture6.png)
![contents](pictrue/picture7.png)
![contents](pictrue/picture8.png)
## 深度学习大模型运行效果展示（二：批量效果运行）
1.初始化数据，提前准备要识别的图片
![contents](pictrue/picture9.png)
2.加载模型并启动程序
![contents](pictrue/picture10.png)
3.运行成功，共花费7秒左右时间识别完所有图片
![contents](pictrue/picture11.png)
4.效果展示
![contents](pictrue/picture12.png)
![contents](pictrue/picture13.png)

## 环境要求

根据requirements.txt，项目依赖以下主要库：

- PyTorch和torchvision：深度学习框架
- OpenCV-Python：图像处理
- NumPy：科学计算
- Matplotlib：可视化
- PyQt5和PyQt5-tools：GUI开发
- Pillow：图像处理
- pandas：数据处理
- tqdm：进度显示
- requests：网络请求
- scipy和seaborn：科学计算和可视化
- YAMLs：配置文件解析

## 工作流程

1. 输入图像或视频
2. 使用YOLOv5模型检测车辆和车牌位置
3. 对检测到的车牌进行透视变换校正
4. 使用专门的车牌识别模型识别车牌号码和颜色
5. 对检测到的车辆使用颜色识别和车型识别模型进行分析
6. 将结果可视化显示在GUI界面上


