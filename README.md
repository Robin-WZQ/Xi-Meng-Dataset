# Chinese-Landscape-Painting-style-Generation

Chinese-Landscape-Painting-style-Generation：Dataset & Method

【I will finish it in a month.】

## Dataset-ALL

Here, we provide the dataset used to train our model. The dataset consists of 489 high-quality traditional Chinese landscape paintings sketch(中国山水画轮廓). All paintings are sized 512x512 and converted to binary format. All paintings are drew by human artists.

Compare with other datasets, These paintings are the first step of drawing a Landscape painting (without any colorization, just lines)

Dataset Samples:
<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/sample-sketch.png width="900"/>
</div>

## Dataset-mini

However, according to my practical experience, use all dataset to train a model(i.e. StlyGAN2) can not generate ideal result. Thus, I devide the dataset into all&mini. In the mini dataset, it inculde 105 sketch paintings whose structure are simpler and easier to let the model learn how to draw.

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



## Style transfer

To make the model obtain the ability of style transfer to any landscape painting style, I use the model from HERE.
Result(not good enough):
<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/t1.png width="800"/>
</div>

To get better result, I use pix2pix model to colorize first and then use the PAMA to do stle transfer task. The reason I do in this way is because PAMA use the VGG pre-trained model which is trained on ImageNet, it can not work well in binary picture. 
Result:

