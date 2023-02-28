# 开题报告(预稿)

## 课题背景及意义(含国内外研究现状综述)

### 研究背景

随着社会的进步与发展，电子技术已经和人类的生活紧紧地相关联。在电气和电子工程领域中，电缆和线缆是不可或缺的组成部分。电子技术的发展离不开电子线缆的发展，线缆在电力输送、信号传输等领域都发挥着重要作用。使用过程中，这些电缆和线缆通常需要弯曲以适应各种应用场景，例如在建筑物、汽车、航空航天、电子设备等领域中。在实际工作环境中，由于布局设计的欠缺、环境结构的变化等因素，会出现线缆弯曲半径过小的情况，这可能会导致电缆或线缆的损坏、磨损、断裂或短路等问题，从而导致电路故障，影响机器正常工作，甚至引起严重的事故;而过大的弯曲半径则会浪费空间、增加成本、降低布线效率等。因此，线缆的弯曲半径是一个非常重要的参数，它决定了电缆或线缆的安装和使用的可靠性、稳定性、耐久性和寿命等。对线缆弯曲半径进行准确地测量和控制非常重要，对指导生产和排除安全隐患具有重大的意义。

### 研究意义

线缆弯曲半径的测量技术的研究和应用具有以下几个方面的意义：

1. 提高电缆或线缆的使用效率：正确地测量线缆的弯曲半径，检测出实际布线当中线缆曲率不合理的地方，给工程师和制造商提供反馈，从而协助更好地控制线缆的设计和制造过程，进而提高电缆或线缆的使用效率，减少不必要的浪费和成本。

2. 提高线缆布线的质量：对于大型的线缆布线项目，准确地测量线缆的弯曲半径可以检验线缆在布线过程中是否符合相关规范和标准，从而提高线缆布线的质量和稳定性。

3. 提高线缆的安全性：线缆过度弯曲可能会导致电缆或线缆的损坏和短路等问题，甚至会引起火灾等严重的安全事故，因此正确地测量线缆的弯曲半径对于保障线缆的安全性非常重要。

综上所述，线缆弯曲半径测量技术的研究和应用对于保障电力系统的安全运行，提高电力系统的效率、稳定性和可靠性和降低电力系统的生产成本等方面具有重要的意义。

### 国内外现状综述

经过多年的发展，线缆弯曲已经有了成熟的测量技术。在传统的领域，主要采用目视法这一传统方法对弯曲半径进行检查。目视检查依靠人眼观察，在直观感觉的基础上结合经验对弯曲半径进行判断。该方法操作简单，检测速度快，现场应用十分方便，可以对大量布线快速粗略判断[1]。另外的, 是使用卡尺， 钢尺等传统工具来辅助专业人员测量弯曲半径[2]。传统测量成本低，方便携带，测量相较于目测法直观、准确。由于一般采用近似圆弧的方法处理，准确度较低，不适用于精度要求较高的场合[3]。而且传统的方法人工介入太多，不利于自动化生产的实现。现代先进的技术是利用光学来测量，通过激光扫描仪、激光干涉仪等光学仪器对线缆弯曲半径进行测量[4]。这种方法能够快速、准确地测量线缆的弯曲半径，但是对于弯曲半径较小的线缆，可能存在一定的误差。还有通过全站仪（total station）测距的方法来测量线缆的弯曲半径，这种方法易于应用，省时，有较高的测量精度，缺点是需要的仪器价格偏高[5]。

机器学习方法与图像处理技术日益成熟。它们能够实现自动化测量，同时具有高精度和可重复性，这对于线缆弯曲半径的测量具有重要的意义。通过数字图像技术，采用滤波技术可以对将环境复杂的图像进行去噪，增强，减少无用信息的干扰，突出感兴趣的对象[6]。机器学习中的深度学习允许由多个处理层组成的计算模型学习具有多个抽象级别的数据表示[7]，使得程序能够自我发现深层次、高级的概念，提取特征。这大大地减轻了人的负担，广泛得应用与图像分割与检测，语言识别等领域。基于深度学习的语义分割旨在为图像中的每个像素分配一个分类标签，对图像理解有重要的作用[8]。根据最近语义分割方法的主要组成部分，可以将它们分为三类：基于区域的语义分割、基于 FCN 的语义分割和弱监督分割[9] [10]。已经有学者采用弱监督半自动图像标记方法[11]应用于分割出可变形线性物体 (DLO)，例如电线、电缆或绳索等，并且设计了可实时分割的实例[12]。

曲线拟合已经有了非常成熟的数学理论和计算机方法，采用插值、回归、样条曲线拟合等方法获得高精度的拟合曲线[13] [14]，能够为可变形线性物体建立一个真实度较高的数学模型进行一步分析。这可以帮助线缆的弯曲半径的进行理论计算。

目前国内外综合运用基于深度学习语义分割和曲线拟合的方法应用于线缆弯曲半径的测量非常少，研究这方面的课题能够提高生产效率，降低生产成本，以及为相应的研究提供参考价值。

## 课题研究主要内容及研究基础

### 课题研究主要内容

线缆在电力输送、信号传输等领域都发挥着重要作用，线缆敷设过程中的弯曲半径控制对线缆的使用寿命有重要影响。项目针对全手动线缆弯曲半径检测过程中效率低，精度差，满足高效生产的需求等问题，应用深度学习语义分割算法实现对线缆特征识别与掩膜分割，在掩膜分割的基础上实现平面线缆的弯曲半径测量，并根据相关标准对线缆弯曲半径做出评价。

要求:

(1) 查阅资料，相关文件资料不少于 20 篇，其中包含至少 10 篇外文资料，结合选题，翻译外文技术资料 5000 汉字以上。

(2) 学习深度学习框架(Pytorch 或 TensorFlow 等)，选择一种较为成熟的深度学习语义分割算法模型、Labelme 标注软件，实现线缆的数据集标注与模型的训练，并得到线缆掩膜；

(3) 使用 Python 或 Matlab 环境下，完成基于掩膜的弯曲半径测量求解方法；

(4) 完成软件设计、开发软件系统，编程和调试运行，编写说明书；

(5) 完成毕业设计说明书(论文)的撰写。

### 研究基础

基于深度学习语义分割的线缆弯曲半径测量技术是一种新型的线缆弯曲半径测量方法，它可以通过使用深度学习算法，自动地对线缆图像进行语义分割，从而精确地测量线缆的弯曲半径。

这种方法的主要优点是能够高效地处理大量的线缆图像，并且可以在无需人工干预的情况下自动完成线缆弯曲半径的测量。具体来说，这种方法的实现需要完成以下几个步骤：

1. 数据采集和预处理：首先需要采集一定数量的线缆图像，并进行预处理，包括图像去噪、平滑和增强等操作，以提高图像质量和减少噪声干扰。

2. 语义分割模型训练：采用深度学习算法，如卷积神经网络（CNN）或分割网络（SegNet），对预处理后的线缆图像进行训练，以学习线缆的特征和轮廓，从而实现语义分割。

3. 弯曲半径测量：在语义分割模型训练完成后，可以使用该模型对新的线缆图像进行语义分割，并提取线缆的轮廓和弯曲程度信息，然后通过数学计算方法来计算线缆的弯曲半径。

相较于传统的线缆弯曲半径测量方法，基于深度学习语义分割的方法具有更高的精度和可靠性，并且能够处理更加复杂的线缆形态和弯曲情况。

## 研究(或调研)方案和思路(技术路线)

### 研究方案

数据采集和预处理：收集不同类型线缆的图像数据集，并对数据进行预处理，包括图像去噪、图像增强和图像标准化等操作。

模型选择和优化：选择适合线缆弯曲半径测量的深度学习语义分割模型，例如 U-Net、SegNet 或 Mask R-CNN 等，并通过调整模型参数和超参数来优化模型。

模型训练和验证：使用采集的数据集对模型进行训练，并使用验证集对模型进行验证，以确保模型的准确性和泛化能力。

线缆弯曲半径计算：利用模型预测的线缆轮廓信息和曲率计算公式，计算线缆的弯曲半径。

结果评估和分析：评估模型预测结果的准确性和稳定性，并进行结果分析和展示。

### 技术路线

[](frame.md ":include :type=markdown")

## 论文框架结构

[](content.md ":include :type=code markmap")

## 参考文献

1. [方武震,姚旭成,赵永鹏等.浅析机载线缆弯曲半径的检测方法[J].电线电缆,2020(06):17-20.DOI:10.16105/j.cnki.dxdl.2020.06.005.](https://kns.cnki.net/kcms2/article/abstract?v=3uoqIhG8C44YLTlOAiTRKibYlV5Vjs7iy_Rpms2pqwbFRRUtoUImHae6S-T5nTIPVZiaD1CMzRQGrCvSgz-A4IVZQmB4vThs&uniplatform=NZKPT&src=copy)

2. [张洁民.电缆弯曲半径的现场简便测量[J].农村电气化,2006(09):17-19.](https://kns.cnki.net/kcms2/article/abstract?v=ZUUpU2TibaLyVMH5RPg3BEh_b42Ky5gDigEJZUunWRpnuhkJLZI8p9tUPPQU1juXT21H2Vyjxx1MZ4Lt5Z9_BwpQDXXTnsVvlTdBzAZebJc=&uniplatform=NZKPT&language=CHS)

3. [一种便捷式弯曲半径测量尺](https://patents.google.com/patent/CN205209412U/zh)

4. [一种电缆弯曲度测量方法](https://patents.google.com/patent/CN105180832A/zh)

5. [Jordal Lars,Vermeer Erwin,Limi Morten,Karlsen Kjetil André. An Alternative Measurement Method to Identify the Minimum Bending Radius of Locked Deformed Bend Restrictor Elements Under Load[P]. ASME 2022 41st International Conference on Ocean, Offshore and Arctic Engineering,2022.](https://kns.cnki.net/kns8/defaultresult/index)

   source: https://asmedigitalcollection.asme.org/OMAE/proceedings-abstract/OMAE2022/V003T04A009/1147718

6. 杨杰,黄朝兵.数字图像处理以及 MATLAB 实现[M].北京:电子工业出版社,2019:75-134

7. [Deep learning](https://www.nature.com/articles/nature14539)

8. [Understanding Convolution for Semantic Segmentation](https://ieeexplore.ieee.org/abstract/document/8354267)

9. [A review of semantic segmentation using deep neural networks](https://link.springer.com/article/10.1007/s13735-017-0141-z)

10. [Methods and datasets on semantic segmentation: A review](https://www.sciencedirect.com/science/article/pii/S0925231218304077)

11. [A Weakly Supervised Semi-Automatic Image Labeling Approach for Deformable Linear Objects](https://ieeexplore.ieee.org/abstract/document/10008018)

12. [RT-DLO: Real-Time Deformable Linear Objects Instance Segmentation](https://ieeexplore.ieee.org/abstract/document/10045806)

13. [洪庆飞. 图像轮廓的 B 样条拟合和优化研究[D].杭州电子科技大学,2021.DOI:10.27075/d.cnki.ghzdc.2021.000406.](https://kns.cnki.net/kcms2/article/abstract?v=3uoqIhG8C475KOm_zrgu4lQARvep2SAkueNJRSNVX-zc5TVHKmDNkhedsxFjM4AUoeXjoYvCV5WpR44fdJYGqz-bguuUIeCL&uniplatform=NZKPT)

14. [NURBS 曲线拟合的最小二乘渐进迭代逼近优化算法](https://kns.cnki.net/kcms2/article/abstract?v=ZUUpU2TibaI8Kag__XNqG-acoYi6a2nynjftp5iePU_BCv9KpZp8P5JVThKt86tZglAli7NMY1O5RGLdeNOhkyCpeDyfZmKc1S8Q9PXV1yk=&uniplatform=NZKPT&language=CHS)
