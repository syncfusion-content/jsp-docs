---
layout: post
title: Legend
description: legend
platform: jsp
control: PivotTreeMap
documentation: ug
---

#Legend

##Legend Visibility

The legend shows the value range differences and color occurrence in the respective leaf node while you hover it with the cursor.

N> By default, the legend is visible in PivotTreeMap.

![](Legend_images/Legend_img1.png)

You can disable the legend by setting the property **showLegend** as **false**. The following code example shows how to disable the legend.

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotTreeMap id="PivotTreeMap1" renderSuccess="RenderSuccess">
//...
</ej:pivotTreeMap>
</div>

<script type="text/javascript">
    function RenderSuccess(args) {
		 var treemapTarget = $('#PivotTreeMap1TreeMapContainer').data("ejTreeMap");
         treemapTarget.model.showLegend = false;
	     treemapTarget.refresh();
	}
</script>

![](Legend_images/Legend_img2.png)