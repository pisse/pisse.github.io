---
layout: post
title:  "linear-gradient"
date:   2016-02-02 21:20:43 +0800
categories: css
---
CSS linear-gradient() 函数创建了一个呈线性渐变颜色的 `<image>`。

线性渐变不是一个css`<color>`且图像不具有内在尺寸；就是说, 它没有默认或者首选的大小或者是比值。它会填充满它所应用的元素。

线性渐变通过一个轴来定义,就是梯度线, 它上面每一个点的颜色都不相同. 垂直于梯度线的线拥有一种单色, 就是梯度线上的一个点的颜色（即垂直的交叉点）。

![渐变梯度线](/assets/img/linear-gradient.png)

## 语法:

    linear-gradient(  [ <angle> | to <side-or-corner> ,]? <color-stop> [, <color-stop>]+ )

    where <side-or-corner> = [left | right] || [top | bottom]
    and <color-stop>       = <color> [ <percentage> | <length> ]?


+   `<side-or-corner>`   <br />
描述渐变线的起始点位置。它包含两个关键词：第一个指出垂直位置left or right，第二个指出水平位置top or bottom。关键词的先后顺序无影响，且都是可选的。<br />
to top(由下到上,默认的方向), to bottom, to left 和 to right这些值会被转换成角度0deg, 180deg, 270deg, 90deg。

+   `<angle>` <br />
用角度值指定渐变的方向（或角度）,**顺时针方向**。


+   `<color-stop>` <br />
颜色值+空格+百分比或长度值。


## 例子:
    linear-gradient( 45deg, blue, red );/* 梯度线45度,由蓝到红的渐变*/
    linear-gradient( to left top, blue, red);/* 梯度线延右低点到左顶点,由蓝到红的渐变*/
    linear-gradient( 0deg, blue, green 40%, red ); /* 梯度线0度(下到上),0-40%处由蓝到绿,40%-end处由绿到红 */


![45度](/assets/img/l-g-1.png)
![右低点到左顶点](/assets/img/l-g-2.png)
![40%](/assets/img/l-g-3.png)


参见:

+   [mozilla-linear-gradient][linear-gradient]

+   [深入理解CSS3 gradient][深入理解CSS3 gradient斜向线性渐变]

+   [css定义语法][css语法]

[linear-gradient]: https://developer.mozilla.org/zh-CN/docs/Web/CSS/linear-gradient
[深入理解CSS3 gradient斜向线性渐变]:   http://www.zhangxinxu.com/wordpress/2013/09/%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3css3-gradient%E6%96%9C%E5%90%91%E7%BA%BF%E6%80%A7%E6%B8%90%E5%8F%98/
[css语法]: https://developer.mozilla.org/zh-CN/docs/Web/CSS/Value_definition_syntax
