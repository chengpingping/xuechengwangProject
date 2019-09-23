# 学成网项目

# 准备

1.素材

2.页面

## css初始化

	*{
		margin: 0;
		padding: 0;
	}
	
	ul{
		list-style: none;
	}
	
	clearfix:after, clearfix:before{
		display: table;
		content: "";
	}
	
	clearfix:after{
		clear: both;
	}
	
	clearfix{
		*zoom: 1;
	}

### 1.clearfix:清除浮动

浮动的框可以向左或向右移动，直到他的边缘碰到包含框或者另外一个浮动框为止。

由于浮动框不在文档的普通流中，所以文档的普通流中的块框表现得像浮动的框不存在一样

脱离文档流的方法：

	position:absolute/fixed;
	float:left;

**浮动的影响**

会导致父元素高度坍塌：父元素中必定有子元素，并且父元素没有设置高度，子元素在父元素中浮动，结果必然会导致父元素高度为零，这就是父元素坍塌的问题。

所以，我们要**清除浮动**

1.在浮动元素后添加一个空标签，然后在css中清除浮动，就可以让父元素自动获取高度：

	clear:both;

优点：代码少，兼容所有的浏览器；

缺点：增加页面的标签，造成结构的混乱；

不推荐使用，已过时。

2.:after伪元素的使用,给浮动的元素的容器添加一个clearfix的class,然后给这个class添加一个:after的伪元素之后添加一个看不见的块级元素清除浮动。

	.clearfix:before,.clearfix:after{
		display:block/table;
		content:"";
	}
	
	.clearfix:after{
		clear:both;
	}
	
	.clearfix{
		*zoom:1;
	}

优点：浏览器支持较好

注意：clearfix这个类需要添加zoom:1（触发haslayout）,才能支持IE6和IE7;

推荐使用，设置公共类，减少css代码

[来源](https://segmentfault.com/a/1190000013664630)

## 确定页面的版心

## 页面布局




