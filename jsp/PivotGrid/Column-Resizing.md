---
layout: post
title:  Column Resizing
description: column resizing
platform: jsp
control: PivotGrid
documentation: ug
---

# Resizing Column

Allows the user to change the column width by holding and dragging the column border using the mouse pointer.

## Column Width Based on Size

The property `enableColumnResizing` adjusts the width of each column based on size of the widget.

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotGrid id="PivotGrid1" enableColumnResizing="true">
	//...
</ej:pivotGrid>
</div>

{% endhighlight %}

## Column Width Based on Text

The `resizeColumnsToFit` property automatically adjusts the width of each column based on the maximum content length available in the respective column.

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotGrid id="PivotGrid1" resizeColumnsToFit="true">
	//...
</ej:pivotGrid>
</div>

{% endhighlight %}

![](Column-Resizing_images/columnresizing.png)