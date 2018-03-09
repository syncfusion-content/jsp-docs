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

Grouping Bar allows user to dynamically alter the report by filter, sort and  remove operations in the PivotGrid control. Based on the Relational datasource and report bound to the PivotGrid control, Grouping Bar will be automatically populated. You can enable Grouping Bar option in PivotGrid by setting the `enableGroupingBar` property to true.

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotGrid id="PivotGrid1" enableGroupingBar="true">
	//...
</ej:pivotGrid>
</div>

{% endhighlight %}

![](Grouping-Bar_images/realtionalclientGB.png)

## Drag and Drop

You can alter the report on fly through drag-and-drop operation.

![](Grouping-Bar_images/GBar_Rel.png)

## Context Menu

You can alter the report by using context menu.

![](Grouping-Bar_images/CMenu_Rel.png)

## Searching Values

Search option available in Grouping Bar allows you to search a specific value that needs to be filtered from the list of values inside the filter pop-up window.

![](Grouping-Bar_images/filter.png)

![](Grouping-Bar_images/groupingbar-search.png)

## Filtering Values

Filtering option available in Grouping Bar allows you to select a specific set of values that needs to be displayed in the PivotGrid control. At least one value needed to be in checked state while filtering otherwise “Ok” button will be disabled.

![](Grouping-Bar_images/FILTER.png)

![](Grouping-Bar_images/FILTER1.png)

## Sorting Values

Sorting option available in Grouping Bar allows you to arrange headers either in ascending or descending order. Sorting option is applicable for fields available only in Row and Column region. By default, headers are sorted in ascending order. Regarding sorting indicator, up arrow denotes ascending order and down arrow denotes descending order.

![](Grouping-Bar_images/sort.png)

![](Grouping-Bar_images/sort-grid.png)

## Removing Field

Remove option available in the Grouping Bar allows you to completely remove a specific field from the PivotGrid control. Remove operation can be either achieved by clicking remove icon available inside each field or by dragging and dropping field out of Grouping Bar region.

![](Grouping-Bar_images/remove.png)

![](Grouping-Bar_images/remove-grid.png) 

