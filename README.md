<div align=center>
    <img src=https://github.com/Robin-WZQ/Xi-Meng/blob/main/assets/logo.png width="600"/>
</div>

# 希孟-数据集
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Love](https://img.shields.io/badge/Made%20with-love-ff69b4)
![Version](https://img.shields.io/badge/version-1.0-red)

## 数据

获若想获取数据请发邮箱至：2485794339@qq.com，并说明您的学校与使用目的，目前我们只对**研究人员**开放，谢谢！

**数据来源** 为了完成轮廓生成和基础色上色任务，我们分别构建了485张由毛笔绘制的纯线条轮廓以及105张“轮廓-基础色”匹配对。纯线条轮廓中，有102张是由艺术家绘制而成，剩余383张轮廓是由现代山水画教材上扫描得来，这些画作均是用毛笔作画而成。另105张“轮廓-基础色”匹配对均是由艺术家绘制而成，每张画先后经历赭石、头青两色的晕染而成，以达到基础色上色的要求。为避免画作中出现的褶皱为模型带来噪声，我们选用在正方形的熟宣卡纸上进行作画。

**预处理** 对于在正方形熟宣上的轮廓和其基础色上色图片，我们直接缩放至512×512。对于在教材上出现的轮廓，我们拍照后进行有重叠的图像剪裁，之后缩放至512×512。由于轮廓图片受光照、纸张颜色以及噪声等影响，直接将其输入模型并不是一个好的选择。因此，我们首先对轮廓图片进行二值化处理。对于“轮廓-基础上色”匹配对，我们进行水平翻转以进行数据增广，因此最终会有210张匹配对。

## 数据样本展示:

轮廓图：
<div align=center>
    <img src=https://github.com/Robin-WZQ/Xi-Meng/blob/main/assets/sketch.png width="600"/>
</div>

匹配图：
<div align=center>
    <img src=https://github.com/Robin-WZQ/Xi-Meng/blob/main/assets/pair.png width="600"/>
</div>

## 致谢

感谢关杜平青绿山水画工作室对画作的支持。👍👍👍



