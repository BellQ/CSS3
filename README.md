# CSS3-border实战
android[查看效果](https://github.com/BellQ/CSS3/blob/master/images/android.png)
机器猫[查看效果](https://github.com/BellQ/CSS3/issues/3)
# border effects
采用CSS3-border创建一些特殊图形[查看效果](https://github.com/BellQ/CSS3/issues/1)
```css
/*拱形*/
.item:nth-child(1) .border-radius {
border-radius: 90px;
}

/*拱形*/
.item:nth-child(2) .border-radius {
border-radius: 90px 90px 0 0;
}

/*半圆*/
.item:nth-child(3) .border-radius {
height: 90px;
border-radius: 90px 90px 0 0;
}

/*左上角*/
.item:nth-child(4) .border-radius {
/*height: 90px;*/
border-radius: 90px 0 0 0;
}

/*四分之一圆*/
.item:nth-child(5) .border-radius {
width: 90px;
height: 90px;
border-radius: 90px 0 0 0;
}

/*横着的椭圆*/
.item:nth-child(6) .border-radius {
height: 90px;
/*border-radius: 50%;*/
border-radius: 90px 90px 90px 90px / 45px 45px 45px 45px;
/*border-radius: 45px / 90px;*/
}

/*竖着的椭圆*/
.item:nth-child(7) .border-radius {
width: 90px;
border-radius: 45px 45px 45px 45px / 90px 90px 90px 90px;
}

/*半个横着的椭圆*/
.item:nth-child(8) .border-radius {
height: 45px;
border-radius: 90px 90px 0 0 / 45px 45px 0 0;
}

/*半个竖着的椭圆*/
.item:nth-child(9) .border-radius {
width: 45px;
border-radius: 45px  0 0 45px / 90px 0 0 90px;
}

/*四分之一竖着的椭圆*/
.item:nth-child(10) .border-radius {
width: 45px;
height: 90px;
border-radius: 45px 0 0 0 / 90px 0 0 0;
}

/*饼环*/
.item:nth-child(11) .border-radius {
width: 40px;
height: 40px;
border: 70px solid red;
border-radius: 90px;
}

/*圆饼*/
.item:nth-child(12) .border-radius {
width: 40px;
height: 40px;
border: 70px solid red;
border-radius: 60px;
}

/*左上角圆饼*/
.item:nth-child(13) .border-radius {
width: 60px;
height: 60px;
border: 60px solid red;
border-radius: 90px 0 0 0;
}

/*对角圆饼*/
.item:nth-child(14) .border-radius {
width: 60px;
height: 60px;
border: 60px solid red;
border-radius: 90px 0 90px 0;
}

/*四边不同色*/
.item:nth-child(15) .border-radius {
width: 0px;
height: 0px;
border-width: 90px;
border-style: solid;
border-color: red green yellow blue;
}

/*右透明色*/
.item:nth-child(16) .border-radius {
width: 0px;
height: 0px;
border-width: 90px;
border-style: solid;
border-color: red green yellow blue;
border-right-color: transparent;
}

/*圆右透明色*/
.item:nth-child(17) .border-radius {
width: 0px;
height: 0px;
border-width: 90px;
border-style: solid;
border-color: red;
border-right-color: transparent;
border-radius: 90px;
}

/*圆右红透明色*/
.item:nth-child(18) .border-radius {
width: 0px;
height: 0px;
border-width: 90px;
border-style: solid;
border-color: transparent;
border-right-color: red;
border-radius: 90px;
}

/*阴阳图前世*/
.item:nth-child(19) .border-radius {
width: 180px;
height: 0px;
border-top-width: 90px;
border-bottom-width: 90px;
border-style: solid;
border-top-color: red;
border-bottom-color: green;
/*border-right-color: red;*/
border-radius: 90px;
}

/*阴阳图前世2*/
.item:nth-child(20) .border-radius {
width: 180px;
height: 90px;
border-bottom-width: 90px;
border-style: solid;
border-bottom-color: green;
background-color: red;
/*border-right-color: red;*/
border-radius: 90px;
}

/*阴阳图今生*/
.item:nth-child(21) .border-radius {
width: 180px;
height: 90px;
border-bottom-width: 90px;
border-style: solid;
border-bottom-color: green;
background-color: red;
border-radius: 90px;
position: relative;
}

.item:nth-child(21) .border-radius::after,
.item:nth-child(21) .border-radius::before {
content: '';
position: absolute;
top: 50%;
width: 20px;
height: 20px;
/*margin: -10px 0 0 0;*/
border-width: 35px;
border-style: solid;
border-radius: 45px;
}

/*左阴阳*/
.item:nth-child(21) .border-radius::after {
background-color: red;
border-color: green;
}

/*右阴阳*/
.item:nth-child(21) .border-radius::before {
background-color: green;
border-color: red;
right: 0;
}

/*右阴阳*/
.item:nth-child(22) .border-radius {
width: 180px;
height: 90px;
border-bottom-width: 90px;
border-bottom-color: green;
border-bottom-style: solid;
background-color: red;
border-radius: 90px;
position: relative;
}

.item:nth-child(22) .border-radius::after,
.item:nth-child(22) .border-radius::before {
content: '';
position: absolute;
top: 50%;
width: 20px;
height: 20px;
border-width: 35px;
border-style: solid;
border-radius: 45px;
}

.item:nth-child(22) .border-radius::before {
border-color: green;
background-color: red;
}

.item:nth-child(22) .border-radius::after {
right: 0;
border-color: red;
background-color: green;
}

/*消息框*/
.item:nth-child(23) .border-radius {
width: 160px;
height: 80px;
background-color: red;
border-radius: 6px;
position: relative;
}

.item:nth-child(23) .border-radius::after {
content: '';
width: 0;
height: 0;
border-width: 10px;
border-style: solid;
border-color: transparent;
border-right-color: red;
position: absolute;
top: 16px;
left: -20px;
}

/*奇怪的图形*/
.item:nth-child(24) .border-radius {
width: 40px;
height: 40px;
border-width: 45px 0 45px 70px;
border-style: solid;
border-radius: 0 0 60px 0;
border-color: red;
}

/*奇怪的图形2*/
.item:nth-child(25) .border-radius {
width: 100px;
height: 40px;
border-width: 45px 20px 45px 70px;
border-style: solid;
border-radius: 60px;
border-color: red;
}

/*QQ对话*/
.item:nth-child(26) .border-radius {
width: 160px;
height: 80px;
background-color: red;
border-radius: 6px;
position: relative;
}

.item:nth-child(26) .border-radius::after {
content: '';
position: absolute;
top: 0;
right: -20px;
width: 30px;
height: 30px;
border-width: 0 0 30px 30px;
border-style: solid;
border-bottom-color: red;
border-left-color: transparent;
border-radius: 0 0 60px 0;
}

/*圆角的百分比设置 */
.item:nth-child(27) .border-radius {
width: 180px;
/*height: 180px;*/
height: 90px;
border-radius: 50%;
border-radius: 90px/45px;

/*百分比是按横竖两个对应的方向的长度进行计算*/

```
