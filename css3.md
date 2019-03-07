---
title: css3
date: 2016-05-09 23:02:16
description: '一下关于css3的效果汇集'
tags: 'css'
categories: '前端'

---

### 鼠标移上去有动画变化，放大等

	.img {
	    -webkit-transform: scale(1.0);
	    -moz-transform: scale(1.0);
	    -o-transform: scale(1.0);
	    -ms-transform: scale(1.0);
	    transform: scale(1.0);
	    -webkit-transition: all .5s eas;
	    -moz-transition: all .5s ease;
	    -o-transition: all .5s ease;
	    -ms-transition: all .5s ease;
	    transition: all .5s ease;
	}
	
	.img : hover {
	    -webkit-transform: scale(1.1);
	    -moz-transform: scale(1.1);
	    -o-transform: scale(1.1);
	    -ms-transform: scale(1.1);
	    transform: scale(1.1);
	    -webkit-transition: all .5s ease;
	    -moz-transition: all .5s ease;
	    -o-transition: all .5s ease;
	    -ms-transition: all .5s ease;
	    transition: all .5s ease;
	}

---

### 淡入淡出

	{
		-webkit-animation-name: fadeIn; /*动画名称*/
		-webkit-animation-duration: 1s; /*动画持续时间*/
		-webkit-animation-iteration-count: 1; /*动画次数*/
		-webkit-animation-delay: 0s; /*延迟时间*/
	}


### 自定义字体到网页中
	一，demo
	<style> 
		@font-face{
			font-family: myFirstFont;
			src: url("SourceHanSansCN-Normal.woff2") format("woff2"),
		         url("SourceHanSansCN-Normal.woff") format("woff"),
		         url("SourceHanSansCN-Normal.ttf") format("truetype"),//Firefox、Chrome、Safari 以及 Opera 支持 .ttf (True Type Fonts)
		         url("SourceHanSansCN-Normal.eot") format("embedded-opentype"),//Internet Explorer 9+仅支持 .eot (Embedded OpenType)
		         url("SourceHanSansCN-Normal.svg") format("svg"),
		         url("SourceHanSansCN-Normal.otf") format("opentype");//Firefox、Chrome、Safari 以及 Opera 支持.otf (OpenType Fonts)
		}
		
		div{
			font-family:myFirstFont;
		}
	</style>
	
	二，@font-face的语法规则：
	@font-face {
	      font-family: <YourWebFontName>;
	      src: <source> [<format>][,<source> [<format>]]*;
	      [font-weight: <weight>];
	      [font-style: <style>];
	    }

	三，@font-face的浏览器字体兼容性
	Webkit/Safari(3.2+)：TrueType/OpenType TT (.ttf) 、OpenType PS (.otf)；
	
	Opera (10+)： TrueType/OpenType TT (.ttf) 、 OpenType PS (.otf) 、 SVG (.svg)；
	
	Internet Explorer： 自ie4开始，支持EOT格式的字体文件；ie9支持WOFF；
	
	Firefox(3.5+)： TrueType/OpenType TT (.ttf)、 OpenType PS (.otf)、 WOFF (since Firefox 3.6)
	
	Google Chrome：TrueType/OpenType TT (.ttf)、OpenType PS (.otf)、WOFF since version 6
	
	由上面可以得出：.eot + .ttf /.otf + svg + woff = 所有浏览器的完美支持。

	四，帮助工具
	https://www.fontke.com/tool/fontface/