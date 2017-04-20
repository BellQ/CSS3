## CSS3 [边框效果](https://github.com/BellQ/CSS3/tree/master/%E8%BE%B9%E6%A1%86%E5%BA%94%E7%94%A8)


## CSS3 [3D转换](https://github.com/BellQ/CSS3/tree/master/3D%E8%BD%AC%E6%8D%A2)

## CSS3 [animation](https://github.com/BellQ/CSS3/tree/master/animation)

## CSS3 基本属性概述
1、	选择器 属性选择器 语法 [] 查找条件是以“属性”做为查找条件，并且我们还可以
	通过属性值来查找 [^=] [$=] [*=] [=] [attr]

	伪类选择器 语法 : E:first-child :last-child :nth-child(n) 
		dl
		dt
		dd 
	dd:nth-child(1)

	n 可以是一个表达式 y = an + b, n 的取值n=0, 1, 2 ...

	伪元素选择器 语法 :: 

	E::before E::after 必须要指定一个 content: '' 新添加的无素是一个行内元素
	根据自已需要 display

	:before :after 尽量使用 :after :before

2、	文字阴影 text-shadow: 2px 2px 5px red; 

3、	边框 
	边框圆角 border-radius: 10px 10px 10px 10px / 10px 10px 10px 10px;
	简写方式
	border-radius: 10px 10px 10px 10px; 水平半径和垂直半径相等
	border-radius: 10px;
	border-radius: 10px 20px;  对角线
	border-radius: 10px 20px 30px; 

	边框阴影
	box-shadow: 2px 2px 5px blue;
	box-shadow: inset 2px 2px 5px blue; 内阴影
	box-shadow: 2px 2px 5px blue, 2px 2px 8px pink;

	边框图片
	border-image-source: url();
	border-image-slice: 27 27 27 27; 
	border-image-repeat: round stretch repeat;
	border-image-width: 30px;

4、	盒模型

	盒子大小 = content + padding + border

	CSS3可以改变这种计算方式

	当设置box-sizing: border-box;
	盒子大小 = width (CSS里设置的width)

	当设置 box-sizing: content-box;
	盒子大小 = content + padding + border


5、	颜色
	
	opacity 子元素会继承
	transparent 完全透明并不调整

	rgba(0, 0, 0, 0.5);

	hsl h色调 0~360度 s饱和度 0%~100% l亮度 0%~100%

6、	线性渐变 径向渐度

	background-img: linear-gradient(to right, yellow 25%, green 50%);

	background-img: radial-gradient(100px at center center, yellow 25%, green 50%);

7、	过渡

	1、必须有两个状态
	2、有触发这两个状态的条件
	3、其中我们练习过程中常用hover来触发，还可修改class

	transition: width 2s, opacity 5s;

	transition-delay: 1s; // 设置延时1s

	transition-timing-function: ease-in; // linear ease ease-in ease-out ease-in-out

	transition: all 1s; // 真在工作当这种用法比较常见

8、	2D转换 3D转换

	缩放scale 移动translate 旋转rotate 倾斜skew

	transform: scale(0.5)

	transform: translate(500px, 500px);

	transform: rotate(180deg);

	transform: skew(x,y); // 没有当成重点去解释，开发中也不常用

	transform: translate(100px, 0) rotate(360deg);

9、	缩放scaleX scaleY scaleZ

	移动translateX translateY translateZ

	旋转rotateX rotateY rotateZ

	transform: translateX;

	transform: rotateX;
	
10、	3D转换
	
	perspective: 1000px;

	设置“近大远小”效果

	transform-style: flat | preserve-3d

	设置给父元素，作用于所有的子元素，子元素必须应用了3D转换

11、	动画
	
	定义一个动画序列
	@keyframes 名字 {
		0% {}
		10% {}
		50% {}
		....
		100% {}
	}

	作用于某个元素时
	animation: 动画序列名称 duration timing-function delay 。。。

12、	background-size 用来设置背景图片大小的

	background-size: 200px | 20%

	background-size: cover; 自动调整缩放比，保证背景图始终铺满整个盒子

	background-size: contain; 自动调整缩放比，保证背景图始终完整显示

13、	伸缩布局
	
	1、指定一个父盒子为伸缩盒子 display: flex;
	2、具备了一个主轴和一个侧轴，并都有方向
	3、主轴 justify-content: flex-start | flex-end | center | space-around | space-between
	4、侧轴 align-items: flex-start | flex-end | center | stretch
	5、强制换行 flex-wrap: nowrap | wrap
	6、调整独立行的对齐 align-content: flex-start | flex-end | center | space-around | space-between
	7、设置子元素的分配比例 flex: 1;
	8、设置某一个子元素在侧轴对齐方式 align-self: flex-start | flex-end | center | stretch
	9、子元素排序 order: 1;
	10、改变主轴的方向及位置 flex-direction: column | row | row-reverse column-reverse	



