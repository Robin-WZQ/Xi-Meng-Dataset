# Chinese-Landscape-Painting-style-Generation

Chinese-Landscape-Painting-style-Generation：Dataset & Method

【I will finish it in a month.】

## Dataset

Here, we provide the dataset used to train our model. The dataset consists of 489 high-quality traditional Chinese landscape paintings sketch(中国山水画轮廓). All paintings are sized 512x512 and converted to binary format. All paintings are drew by human artists.

Compare with other datasets, These paintings are the first step of drawing a Landscape painting (without any colorization)

Dataset Samples:
<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/sample-sketch.png width="900"/>
</div>

## Generation

Use the StyleGAN3 model, generation example:
<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/g1.jpg width="600"/>
</div>

<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/g2.jpg width="600"/>
</div>


## Style transfer

To make the model obtain the ability of style transfer to any landscape painting style, I use the model from HERE.
Result:
<div align=center>
    <img src=https://github.com/Robin-WZQ/Chinese-Landscape-Painting-style-Generation/blob/main/assets/t1.png width="800"/>
</div>
