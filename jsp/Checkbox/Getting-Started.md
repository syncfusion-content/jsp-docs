---
layout: post
title: getting-started
description: getting started for CheckBox
platform: JSP
control: CheckBox
documentation: ug
---

# GettingStarted

This section briefly describes about how to create a checkbox in your application with JSP.

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
<title>Check Box</title>
<style>
  td {
            padding: 5px;
        }
</style>
</head>
<body>
<div  >
<div>
<div>
<br /> Hobbies <br /> <br />
<table>
<tr>
<td>
<ej:checkBox id="check1" checked="true" size="small"></ej:checkBox>
<label for="check1">Music</label></td>
<td colspan="2" >
<ej:checkBox id="Checkbox3" checked="true" size="small" ></ej:checkBox>
<label for="Checkbox3" >Sports</label></td>
<td colspan="2">
<ej:checkBox id="Checkbox4" size="small" ></ej:checkBox>
<label for="Checkbox4" >Bike Riding</label></td></tr></table>
<br /> <br /> Favorite Search Engines <br /> <br />
<table>
<tr>
<td> <ej:checkBox id="Checkbox1" checked="true" size="medium"></ej:checkBox>
<label for="Checkbox1" >Google</label></td>
<td colspan="2"> <ej:checkBox id="Checkbox5"  checked="true" size="medium"></ej:checkBox>
<label for="Checkbox5" >Yahoo</label></td>
<td colspan="2" > <ej:checkBox id="Checkbox6" size="medium" ></ej:checkBox>
<label for="Checkbox6" >Bing</label></td>
</tr>
</table>
<br /> <br /> Favorite Social networks <br /> <br />
<table>
<tr>
<td >
<ej:checkBox id="Checkbox2" enableTriState="true" size="medium" checkState="indeterminate"></ej:checkBox>
<label for="Checkbox2" >Facebook</label></td>
<td colspan="2">
<ej:checkBox id="Checkbox7" enableTriState="true" size="medium" checkState="indeterminate"></ej:checkBox>
<label for="Checkbox7" >GPlus</label></td>
<td colspan="2">
<ej:checkBox id="Checkbox8" enableTriState="true" size="medium" checkState="indeterminate"></ej:checkBox>
<label for="Checkbox8" >Twitter</label></td>
</tr>
</table>
<br />
</div>
</body>
</html>


{% endhighlight %}

You can execute the above code example to display the CheckBox control.

![](getting-started_images/Checkbox.png) 
