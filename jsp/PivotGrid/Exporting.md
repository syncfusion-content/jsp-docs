---
layout: post
title: Exporting
description: exporting
platform: jsp
control: PivotGrid
documentation: ug
---

# Exporting

The PivotGrid control can be exported to the following file formats.

* Excel
* Word
* PDF
* CSV

The PivotGrid control can be exported by invoking **“exportPivotGrid”** method, with an appropriate export option as parameter.

## JSON Export

### Excel Export

User can export the contents of PivotGrid to an Excel document for future archival, references and analysis purposes.

To achieve Excel export, URL and file name is sent as the parameter.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="exportButtonClick" showRoundedCorner="true" size="large" text="Export"></ej:button> 
    </div>
    
	<script type="text/javascript">
		function exportButtonClick(args) {
                var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
                pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport","fileName");
            }
	</script>

{% endhighlight %} 

### Word Export

User can export the contents of PivotGrid to a Word document for future archival, references and analysis purposes.

To achieve Word export, URL and file name is sent as the parameter.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="exportButtonClick" showRoundedCorner="true" size="large" text="Export"></ej:button> 
    </div>
    
	<script type="text/javascript">
		function exportButtonClick(args) {
                var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
                pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport","fileName");
            }
	</script>

{% endhighlight %} 

### PDF Export

User can export the contents of PivotGrid to a PDF document for future archival, references and analysis purposes.

To achieve Word export, URL and file name is sent as the parameter.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="exportButtonClick" showRoundedCorner="true" size="large" text="Export"></ej:button> 
    </div>
    
	<script type="text/javascript">
		function exportButtonClick(args) {
                var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
                pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport","fileName");
            }
	</script>

{% endhighlight %} 

### CSV Export

User can export the contents of PivotGrid to a CSV document for future archival, references and analysis purposes.

To achieve CSV export, URL and file name is sent as the parameter.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="exportButtonClick" showRoundedCorner="true" size="large" text="Export"></ej:button> 
    </div>
    
	<script type="text/javascript">
		function exportButtonClick(args) {
                var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
                pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport","fileName");
            }
	</script>

{% endhighlight %} 

### Customize the export document name

For customizing file name, we need to send file name as parameter to the **“exportPivotGrid”**  method along with method name.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="exportButtonClick" showRoundedCorner="true" size="large" text="Export"></ej:button> 
    </div>
    
	<script type="text/javascript">
		function exportButtonClick(args) {
                var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
                pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport","fileName");
            }
	</script>

{% endhighlight %} 


## Exporting Customization

You can add title and description to the exporting document by using the title and description properties respectively obtained in the `beforeExport` event. Similarly, you can enable or disable styling on the exported document by using the `exportWithStyle` property.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1" beforeExport="BeforeExport">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="exportButtonClick" showRoundedCorner="true" size="large" text="Export"></ej:button> 
    </div>
    
	<script type="text/javascript">
        function BeforeExport(args) {
			args.title = "PivotGrid";
            args.description = "Displays both OLAP and Relational datasource in tabular format";
			args.exportWithStyle = false;   // by default it sets as true. It improves performance on exporting huge data when it sets as false.
	    }
		function exportButtonClick(args) {
                var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
                pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport","fileName");
            }
	</script>

{% endhighlight %} 

### Exporting complete data on Paging

When paging is enabled, you can export the complete data by enabling the `enableCompleteDataExport` property. It is supported in both types of JSON and PivotEngine export and it is applicable for all kinds of exporting formats available in PivotGrid.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1" beforeExport="BeforeExport" enableCompleteDataExport="true">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="exportButtonClick" showRoundedCorner="true" size="large" text="Export"></ej:button> 
    </div>
    
	<script type="text/javascript">
        function BeforeExport(args) {
			args.title = "PivotGrid";
            args.description = "Displays both OLAP and Relational datasource in tabular format";
			args.exportWithStyle = false;   // by default it sets as true. It improves performance on exporting huge data when it sets as false.
	    }
		function exportButtonClick(args) {
                var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
                pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport","fileName");
            }
	</script>

{% endhighlight %}

The below screenshot shows the PivotGrid control exported to Excel document.

![](Exporting_images/ExportPivotExcel.png)

The below screenshot shows the PivotGrid control exported to Word document.

![](Exporting_images/ExportPivotWord.png)

The below screenshot shows the PivotGrid control exported to PDF document.

![](Exporting_images/ExportPivotPDF.png)

The below screenshot shows the PivotGrid control exported to CSV document.

![](Exporting_images/ExportPivotCSV.png)

