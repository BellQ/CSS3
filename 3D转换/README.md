# 3D转换的应用
文字翻转的核心代码
```css
.text-box {
			margin-top: 100px;
			text-align: center;
			line-height: 1;
			font-size: 100px;
			/*color: #065DAC;*/
		}

		.text-box span {
			display: inline-block;
			position: relative;
		}

		.text-box span::before,
		.text-box span::after {
			content: attr(data-text);
			position: absolute;
			left: 0;
			top: 0;
			transition: all 1s;
			transform-origin: left center;
		}

		.text-box span::before {
			z-index: 3;
			color: #FFF;
			transform: rotateY(-15deg);
		}

		.text-box span::after {
			z-index: 2;
			color: rgba(0, 0, 0, 0.3);
		}

		.text-box:hover span::before {
			transform: rotateY(-40deg) skew(0, 5deg);
		}

		.text-box:hover span::after {
			transform: skew(0, 20deg);
		}
```
