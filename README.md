# Chinese-Landscape-Painting-style-Generation

Chinese-Landscape-Painting-style-Generation：Dataset & Method


![图片2](https://github.com/Robin-WZQ/Chinese-Landscape-Painting-Generation/blob/main/assets/test.gif)

## Dataset-ALL

Here, we provide the dataset used to train our model. The dataset consists of 489 high-quality traditional Chinese landscape paintings sketches(中国山水画轮廓). All paintings are resized to 512x512 and converted to binary format. All paintings are drew by human artists.

Compare with other datasets, These paintings are the first step of drawing a Landscape painting (without any colorization, just lines)

Dataset Samples:
<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/sample-sketch.png width="900"/>
</div>

## Dataset-mini

However, according to my practical experience, use all dataset to train a model(i.e. StyleGAN2) can not generate ideal results. Thus, I divide the dataset into all&mini. In the mini dataset, it inculdes 105 sketches whose structure are simpler and easier to let the model learn how to draw.

Each of the 105 sketch has a corresponding painted painting. Thus it also can be used as the train dataset for colorized model(i.e. Pix2Pix). And I also use filp-tranverse to do data expansion. So there will be 210 sketch-paintings pair in the end.

## Generation

Use the StyleGAN2 model, generation example:
<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/g1.jpg width="600"/>
</div>

<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/g2.jpg width="600"/>
</div>

## Colorization

Use the pix2pix model, generation example:

<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/pic1.png width="600"/>
</div>

## Style transfer

To get better result, I use pix2pix model to colorize first and then use the PAMA to do style transfer task. The reason I do in this way is because PAMA use the VGG pre-trained model which is trained on ImageNet, it can not work well in binary picture. 

Final result:

<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/t1.png width="800"/>
</div>



