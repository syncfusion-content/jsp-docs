---
layout: post
title: Legend
description: legend
platform: jsp
control: PivotChart
documentation: ug
---

# Legend

## Legend Visibility

You can enable or disable legend using the `visible` property inside the `legend` object.

N> By default, the legend is visible in PivotChart.

{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img1.png) 

## Legend Shape
You can customize the legend `shape` in PivotChart control. Default value of legend shape is “Rectangle”. Following legend shapes that are supported:

* Rectangle
* Circle
* Cross
* Diamond
* Pentagon
* Hexagon
* Star
* Ellipse
* Triangle etc.

{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
			args.model.legend.shape = "star";
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img2.png) 

## Legend Position
By using the `position` property, you can place the legend at top, bottom, left or right of the PivotChart. 

N> Default value of legend position is "bottom" in PivotChart.

{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
			args.model.legend.position = "top";
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img3.png) 

## Legend Title
To add the legend title, you have to specify the title text in `title.text` property.

{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
			args.model.legend.title.text = "Countries";
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img4.png) 

## Legend Alignment
You can align the legend to center, far and near based on its position in the Chart area using the `alignment` option.
 
{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
			args.model.legend.alignment = "near";
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img5.png)

## Legend Items - Size and Border
By using the legend `itemStyle.width`, `itemStyle.height` and `itemStyle.border` properties, you can change the legend items - size and border.

{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
			args.model.legend.itemStyle.border.color = "magenta";
			args.model.legend.itemStyle.border.width = 1.5;
			args.model.legend.height = 12;
			args.model.legend.width = 12;
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img6.png)
 
## Legend Border
By using the `border` option in legend, you can customize border color and width.

{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
			args.model.legend.border.color = "#FFC342";
			args.model.legend.border.width = 2;
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img7.png)

## Legend Text
By using the `font` option, you can customize the font family, font style, font weight and size of the legend text. 

{% highlight html %}

	<div>
		<ej:pivotChart id="PivotChart1 load="onLoad">
		//...
		</ej:pivotChart
	</div>
	<script type="text/javascript">
		function onLoad(args) {
			//...
			args.model.legend.visible = true;
			args.model.legend.font.fontFamily = "Segoe UI";
			args.model.legend.font.fontWeight = "bold";
			args.model.legend.font.fontStyle = "italic";
		}
	</script>

{% endhighlight %}

![](Legend_images/Legend_img8.png)