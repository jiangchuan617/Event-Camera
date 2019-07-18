# Unsupervised Event-based Learning of Optical Flow, Depth, and Egomotion

## 摘要

propose a novel framework for unsupervised learning for event cameras that learns motion information from only the event stream.

we pass through a neural network to predict the motion of the events.

the motion is used to attempt to remove any motion blur in the event image.

train two networks with this framework, one to predict optical flow, and one to predict egomotion and depths,

多车辆立体事件相机数据集上评估这些网络，以及来自各种不同场景的定性结果。

## 介绍

提出 a novel input representation that captures the full spatiotemporal distribution of the events, 

提出and a novel set of unsupervised loss functions that allows for efﬁcient learning of motion information from only the event stream.

图2 ：光流和运动和深度网络的网络架构。在光流网络中，仅使用编码器 - 解码器部分，而在运动和深度网络中，编码器 - 解码器用于预测深度，而姿势模型预测运动。在训练时，在连接到网络的下一级之前，在解码器的每个阶段应用损失

- 一种新的离散事件体积表示形式,用于将事件传递到神经网络中。
- 基于运动模糊损失函数的新颖应用,仅允许从事件无监督地学习运动信息
- 一种新型的立体相似性损耗应用于一对去模糊事件图像的普查变换
- 对多车辆立体事件摄像机数据集 [26] 进行定量评估,从各种夜间和其他具有挑战性的场景中进行定性和定量评估

## 方法

3.1 通过完全卷积神经网络来预测流量和/或运动和深度。然后，我们使用预测的运动来尝试对事件进行去模糊，并应用最小化去模糊图像中的模糊量的损失，如第2节中所述。

 3.2。这种损失可以直接应用于我们的光流网络。

 3.3。对于运动和深度网络，我们描述了在第二节中转换为光流。 

 3.4.1 以及Sec中的新颖立体声差异丢失。

 3.4.2。我们的架构总结在图2中。