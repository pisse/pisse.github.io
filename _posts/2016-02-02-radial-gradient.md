---
layout: post
title:  "radial-gradient"
date:   2016-02-14 15:20:43 +0800
categories: css frontend
---
CSS radial-gradient() 函数创建了一个呈径向渐变颜色的 `<image>`。

线性渐变不是一个css`<color>`且图像不具有内在尺寸；就是说, 它没有默认或者首选的大小或者是比值。它会填充满它所应用的元素。

径向渐变(Radial gradients)由其中心点、边缘形状轮廓及位置、色值结束点（color stops）定义而成。径向渐变的中心至边缘由连续的同心轮廓组成,轮廓由边缘形状设定,仅可为圆或椭圆。
色值结束点用于设定虚拟渐变射线（virtual gradient ray）的变化方式，由中心点水平变化至右侧（如图）。

![渐变梯度线](/assets/img/radial-gradient.png)

## 语法:

    radial-gradient( [ circle || <length> ] [ at <position> ]? ,
    | [ ellipse || [<length> | <percentage> ]{2}] [ at <position> ]? ,
    | [ [ circle | ellipse ] || <extent-keyword> ] [ at <position> ]? ,
    | at <position> ,
    <color-stop> [ , <color-stop> ]+ )

    // 定义轮廓, 大小,位置和颜色值
    <extent-keyword> = closest-corner | closest-side | farthest-corner | farthest-side
    <color-stop> = <color> [ <percentage> | <length> ]?



+   `<position>`   <br />
`<position>`与background-position或者transform-origin类似。如缺省，默认为中心点。

+   `<shape>` <br />
渐变的形状。圆形（渐变的形状是一个半径不变的正圆）或椭圆形（轴对称椭圆）。默认值为椭圆。

+   `<size>`
渐变的尺寸大小。

+   `<color-stop>` <br />
颜色值+空格+百分比或长度值。


## 例子:
    /* 轮廓形状为椭圆,长半径150px,短半径50px,中心在(45px,45px),0-50%处由#00FFFF到绿色,50%-90%绿色到#0000FF,90%-end为#0000FF*/
    radial-gradient(ellipse 150px 50px at 45px 45px , #00FFFF 0%, green 50%, #0000FF 90%);

    /* 轮廓形状为圆,轮廓边缘经过离中心最远角,中心在(45px,45px),由#FF0000到#0000FF*/
    radial-gradient(farthest-corner at 45px 45px , #FF0000 0%, #0000FF 100%);

    /* 轮廓形状为圆,中心在(60px,50%),0-14px处由#0000FF到#FF0000,14px-end为#FF0000, */
    radial-gradient(16px at 60px 50% , #0000FF 0%, #FF0000 14px);


![45度](/assets/img/r-g-1.png)


参见:

+   [mozilla-radial-gradient][radial-gradient]

+   [css定义语法][css语法]

[radial-gradient]: https://developer.mozilla.org/zh-CN/docs/Web/CSS/radial-gradient
[css语法]: https://developer.mozilla.org/zh-CN/docs/Web/CSS/Value_definition_syntax
