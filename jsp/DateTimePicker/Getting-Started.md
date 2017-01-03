---
layout: post
title: getting-started
description: getting started for Date Time Picker
platform: JSP
control: Date Time Picker
documentation: ug
---

# GettingStarted

This section briefly describes about how to create a Date Time Picker in your application with JSP.

## Create a simple CheckBox in JSP

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
<title>Date Time Picker</title>
<style>
.control{
margin-top: 15%;
}
</style>
</head>
<div >
<div class="control" margin=”auto” align=”center”>
<ej:dateTimePicker id="datetimepicker"  width="50%" ></ej:dateTimePicker>
</div>
</div>
</html>

{% endhighlight %}

You can execute the above code example to display the CheckBox control.

![](getting-started_images/Datetimepicker.png) 

### Configuring Date Time Picker

This section encompasses the details on how can you configure the Date Time picker control in your application and customize it with various properties for date time picker according to your requirement.

To modify the mindatetime and maxdatetime, add the following code in your JSP file.

{% highlight html %}


<ej:dateTimePicker id="datetimepicker" minDateTime="12/01/2016 09:00 AM"  maxDateTime="12/30/2016 09:00 PM" width=”30%”></ej:dateTimePicker>


{% endhighlight %}

The following screenshot illustrates the Color Picker control with preset type property.

![](getting-started_images/Datetime Picker.png)
