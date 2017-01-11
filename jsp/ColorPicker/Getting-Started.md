---
layout: post
title: Getting-started
description: Getting started for ColorPicker
platform: JSP
control: ColorPicker
documentation: ug
---

# GettingStarted

This section briefly describes about how to create a ColorPicker in your application with JSP.

The useage of the ColorPicker is described in the following sections.

## Create a simple ColorPicker in JSP

Please refer this page http://help.syncfusion.com/jsp/overview for the general information regarding integerating Syncfusion widgets.

Create a JSP file and add the below given code to render the checkbox control. 

{% highlight javascript %}

<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
   pageEncoding="ISO-8859-1"%>
<%@ taglib prefix="ej" uri="/WEB-INF/EJ.tld"%>
<%@ page import="com.syncfusion.*"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<script type="text/javascript" src="Scripts/jquery-3.1.1.min.js"></script>
<link href="Content/ejthemes/material/ej.web.all.min.css" rel="stylesheet" />
<script type="text/javascript" src="Scripts/ej.web.all.min.js"></script>
<title>ColorPicker</title>
<style>
 .control{
margin-left: 10%;
}

.cols-sample-area {
		width: 100%;
}
</style>
</head>
<div class="cols-sample-area">
<div class="control">
<ej:colorPicker id="color" value="#278787" modelType="palette"> </ej:colorPicker>
</div>
</div>
</html>

{% endhighlight %}

You can execute the above code example to display the ColorPicker control with simple control list.

![](getting-started_images/colorpicker.png) 

### Configuring ColorPicker

This section encompasses the details on how can you configure the ColorPicker control in your application and customize it with various properties such as preset type for ColorPicker according to your requirement.

To modify the preset type of the ColorPicker, add the following code in your JSP file.

{% highlight javascript %}

<ej:colorPicker id="color" value="#278787" modelType="palette" presetType="CandyCrush" ></ej:colorPicker>

{% endhighlight %}

The following screenshot illustrates the ColorPicker control with preset type property.

![](getting-started_images/colorpickerpreset.png) 

