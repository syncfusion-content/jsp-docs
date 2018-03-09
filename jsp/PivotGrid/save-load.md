---
layout: post
title: Save and Load Report
description: save and load report
platform: jsp
control: PivotGrid
documentation: ug
---

# Save and Load Report

Allows you to save the current report of PivotGrid and render the control with the saved report later.

## Save Report to Local Storage

To save the current report of PivotGrid to local storage, we need to call the `saveReport` method in PivotGrid.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1" saveReport="saveReport">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="saveLocal" showRoundedCorner="true" size="large" text="Save To Local"></ej:button> 
    </div>
    
	<script type="text/javascript">
    	function saveReport(){
            url = "",
            name = "report",
            storage = "local",
            pGridObj.saveReport(name, storage, url);
        }        
        function saveToLocal(args){
            localStorage.setItem("report", JSON.stringify(args.report));
        }
	</script>

{% endhighlight %}

## Load Report from Local Storage

To load the stored report of PivotGrid from local storage, we need to call the `loadReport` method in PivotGrid.

{% highlight html %}

	<div>
		<ej:pivotGrid id="PivotGrid1" loadReport="loadReport">
		//...
		</ej:pivotGrid
	</div>
    <div>
        <ej:button id="button" click="saveLocal" showRoundedCorner="true" size="large" text="Save To Local"></ej:button> 
    </div>
    
	<script type="text/javascript">
    	function loadReport(){
            url = "",
            name = "report",
            storage = "local",
            pGridObj.loadReport(name, storage, url);
        }       
        function loadFromLocal(args){
            args.targetControl.model.dataSource = JSON.parse(localStorage.getItem("report"));
        }
	</script>

{% endhighlight %}