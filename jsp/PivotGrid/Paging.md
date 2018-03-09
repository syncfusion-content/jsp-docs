---
layout: post
title: Paging
description: paging
platform: jsp
control: PivotGrid
documentation: ug
---

# Paging

## Pager 

Paging helps to improve the rendering performance of the PivotGrid control by dividing large amount of data into sections and displaying one section at a time. You can enable Paging option in PivotGrid by setting the `enablePaging` property to true. You can provide the page size and current page details for each axis in `pagerOptions` property.

You need to initialize the widget using **ejPivotPager** tag. Inside the **ejPivotPager** tag, the enumeration property mode needs to be set to **ej.PivotPager.Mode.Both** in-order to display both categorical pager and series pager. The other enumerations such as **ej.PivotPager.Mode.Categorical** and **ej.PivotPager.Mode.Series** will display only categorical pager and series pager respectively.

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotGrid id="PivotGrid1" load="onLoad" enablePaging="true">
	//...
</ej:pivotGrid>
<ej:pivotPager id="PivotPager" mode="both" targetControlID="PivotGrid1"></ej:pivotPager>
</div>
<script type="text/javascript">

    function onLoad(args) {
		args.model.dataSource.pagerOptions= {
                                    categoricalPageSize: 5,
                                    seriesPageSize: 5,
                                    categoricalCurrentPage: 1,
                                    seriesCurrentPage: 1
                                };
	}
</script>

{% endhighlight %} 

Following are the navigation options available in Pager.

* Move First - Navigates to the first page.
* Move Last - Navigates to the last page. 
* Move Previous - Navigates to the previous page from the current page.
* Move Next - Navigates to the next page from the current page.
* Numeric Box - Navigates to the desired page by entering an appropriate page number in numeric value.

![](Paging_images/paging.png)


## Virtual Scrolling

Virtual Scrolling is a technique that allows user to view the PivotGrid information page by page with the use of vertical and horizontal scrollbar. You can enable Virtual Scrolling option in PivotGrid by setting the `enableVirtualScrolling` property to true. You can provide the page size and current page details for each axis in `pagerOptions` property. 

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotGrid id="PivotGrid1" load="onLoad" enableVirtualScrolling="true">
	//...
</ej:pivotGrid>
</div>
<script type="text/javascript">

    function onLoad(args) {
		args.model.dataSource.pagerOptions= {
                                    categoricalPageSize: 5,
                                    seriesPageSize: 5,
                                    categoricalCurrentPage: 1,
                                    seriesCurrentPage: 1
                                };
	}
</script>

{% endhighlight %} 

![](Paging_images/virtual-scrolling.png)

## Page Settings

The properties associated to paging are:

* enablePaging – This property is used to enable/disable paging in PivotClient control.
* pagerOptions.categoricalPageSize - Specifies the number of categorical columns to be displayed within a page of the PivotClient control.
* pagerOptions.seriesPageSize - Specifies the number of series rows to be displayed within a page of the PivotClient control.
* pagerOptions.categoricalCurrentPage - Sets the current page of the categorical axis in PivotClient control.
* pagerOptions.seriesCurrentPage - Sets the current page of the series axis in PivotClient control.

Page setting for categorical and series axes are mandatorily needed to be set in data source property by using the following properties.

{% highlight html %}

<div class="cols-sample-area">
<ej:pivotGrid id="PivotGrid1" load="onLoad" enablePaging="true">
	//...
</ej:pivotGrid>
<ej:pivotPager id="PivotPager" mode="both" targetControlID="PivotGrid1"></ej:pivotPager>
</div>
<script type="text/javascript">

    function onLoad(args) {
		args.model.dataSource.pagerOptions= {
                                    categoricalPageSize: 5,
                                    seriesPageSize: 5,
                                    categoricalCurrentPage: 1,
                                    seriesCurrentPage: 1
                                };
	}
</script>

{% endhighlight %} 