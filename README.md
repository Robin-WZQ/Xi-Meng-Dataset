<div align=center>
    <img src=https://github.com/Robin-WZQ/Xi-Meng-Dataset/blob/main/assets/logo.png width="600"/>
</div>

# Xi Meng-Datasets
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Love](https://img.shields.io/badge/Made%20with-love-ff69b4)
![Version](https://img.shields.io/badge/version-1.0-red)

[中文](https://github.com/Robin-WZQ/Xi-Meng-Dataset) | [English](https://github.com/Robin-WZQ/Xi-Meng-Dataset/tree/english)

## Data

If you want to get the data, please email to: 2485794339@qq.com , and explain your school and use purpose. **Note that we are only open to researchers**. Thank you!

**Data source：** in order to complete the tasks of contour generation and basic color coloring, we constructed 485 pure line contours drawn by brush and 105 "contour -- basic color" matching pairs respectively. Among the pure line outlines, 102 are drawn by artists, and the remaining 383 are scanned from modern landscape painting textbooks. These paintings are painted with brush. The other 105 matching pairs of "Outline - basic color" are all drawn by artists. Each picture has experienced the halo dyeing of ochre and head green, so as to meet the requirements of basic color coloring. In order to avoid the noise caused by the folds in the painting, we choose to draw on the square cooked poster paper.

**Preprocessing：** for the outline on the square and its base color picture, we directly zoom to 512 × 512。 For the outline appearing in the textbook, we cut the overlapping image after taking photos, and then zoom to 512 × 512。 Because the contour image is affected by illumination, paper color and noise, it is not a good choice to input it directly into the model. Therefore, we first binarize the contour image. For "contour base color" matching, we flip horizontally to expand the data, so there will be 210 matching pairs in the end.

## Sample

Contour：
<div align=center>
    <img src=https://github.com/Robin-WZQ/Xi-Meng-Dataset/blob/main/assets/sketch.png width="600"/>
</div>

Contour -- basic color:
<div align=center>
    <img src=https://github.com/Robin-WZQ/Xi-Meng-Dataset/blob/main/assets/pair.png width="600"/>
</div>

## Acknowledge

Thanks to Guan duping's green landscape painting studio(关杜平青绿山水画工作室) for its support.👍👍👍



