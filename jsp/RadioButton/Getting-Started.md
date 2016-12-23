---
layout: post
title: getting-started
description: getting started for RadioButton
platform: JSP
control: RadioButton
documentation: ug
---

# GettingStarted

This section briefly describes about how to create a radio button in your application with JSP.

## Create a simple RadioButton in JSP

Please refer the page https://help.syncfusion.com/jsp/overwiew for the general information regarding ingerating syncfusion widgets.

Create a JSP file and add the below mentioned code to render the radio button control.

{% highlight javascript %}

<%@ page language="java" contentType="text/html; charset=ISO-8859-1"
   pageEncoding="ISO-8859-1"%>
<%@ taglib prefix="ej" uri="/WEB-INF/EJ.tld"%>
<%@ page import="com.syncfusion.*"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>Radio Button</title>
<script type="text/javascript" src="Scripts/jquery-3.1.1.min.js"></script>
<link href="Content/ejthemes/material/ej.web.all.min.css" rel="stylesheet" />
<script type="text/javascript" src="Scripts/ej.web.all.min.js"></script>
</head>
<body>
<div>
Category<br> <br>
<table>
<tr>
<td>
<ej:radioButton id="radio1" name="Category" size="small" value="fresher" ></ej:radioButton> 
<label for="radio1">Fresher</label>
</td>
<td colspan="2">
<ej:radioButton id="radio2" name="Category" size="small" value="experienced" checked="true" ></ej:radioButton> 
<label for="radio2">Experienced</label>
</td>
</tr>
</table><br>
Experience
<table>
<tr>
<td>
<ej:radioButton id="radio3" name="experienced" size="medium" value="1+years" checked="true" ></ej:radioButton> 
<label for="radio3">1+ Years</label>
</td>
<td colspan="2">
<ej:radioButton id="radio4" name="experienced" size="medium" value="2.5+ Years" ></ej:radioButton>
<label for="radio4">2.5+ Years</label>
</td>
<td colspan="2">
<ej:radioButton id="radio5" name="experienced" size="medium" value="5+ years" ></ej:radioButton>
<label for="radio5">5+ Years</label>
</td>
</tr>
</table>
</div>
</body>
</html>

{% endhighlight %}

You can execute the above code example to display the Radio Button control .

![](getting-started_images/radiobutton.png) 
