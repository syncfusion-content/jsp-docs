---
layout: post
title: Grouping Bar
description: grouping bar
platform: jsp
control: PivotGrid
documentation: ug
---

# Grouping Bar

## Initialization

Grouping Bar allows user to dynamically alter the report by filter and remove operations in the PivotGrid control. Based on the OLAP datasource and report bound to the PivotGrid control, Grouping Bar will be automatically populated. You can enable Grouping Bar option in PivotGrid by setting the `enableGroupingBar` property to true.

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotGrid id="PivotGrid1" enableGroupingBar="true">
	//...
</ej:pivotGrid>
</div>

{% endhighlight %}

![](Grouping-Bar_images/OlapGroupingbar.png)

## Drag and Drop

You can alter the report on fly through drag-and-drop operation.

![](Grouping-Bar_images/GBar_Olap.png)

## Context Menu

You can also alter the report by using context menu.

![](Grouping-Bar_images/CMenu_Olap.png)

## Searching Values

Search option available in Grouping Bar allows you to search a specific value that needs to be filtered from the list of values inside the filter pop-up window.

![](Grouping-Bar_images/OlapFilterIcon.png)

![](Grouping-Bar_images/olapclientsearching.png)

## Filtering Values

Filtering option available in Grouping Bar allows you to select a specific set of values that needs to be displayed in the PivotGrid control. At least one value needed to be in checked state while filtering otherwise “Ok” button will be disabled.

![](Grouping-Bar_images/OlapFiltericon.png)

![](Grouping-Bar_images/OlapFiltering.png)

## Removing Field

Remove option available in the Grouping Bar allows you to completely remove a specific field from the PivotGrid control. Remove operation can be either achieved by clicking remove icon available inside each field or by dragging and dropping field out of Grouping Bar region.

![](Grouping-Bar_images/OlapRemoveicon.png)

![](Grouping-Bar_images/OlapRemove.png) 

