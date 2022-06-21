---
layout: post
title: Getting Started with JSP DatePicker Control | Syncfusion
description: Learn here about getting started with Syncfusion Essential JSP DatePicker Control, its elements, and more.
platform: JSP
control: DatePicker
documentation: ug
---
# Getting Started with JSP DatePicker

This section explains briefly about how to create a **DatePicker** in your application with JSP.

The usage of **DatePicker** control is described in the following sections.

## Create a DatePicker in JSP
You can create an JSP application and add necessary scripts with the help of the given [JSP Getting Started Documentation](/jsp-docs/jsp/Getting-Started).


Create the JSP file and add the below given code to render **DatePicker** control.

{% highlight html %}

        <div>DatePicker control in JSP</div>
        <ej:datePicker id="datepicker" ></ej:datePicker>
        
{% endhighlight %}

You can execute the above code example to display the **DatePicker** control.

![JSP DatePicker getting started](Getting Started-images/Datepicker_image1.png) 

## Configuring DatePicker
This section encompasses the details on how you can setting the **MinDate**, **MaxDate** properties with **DatePicker** control in your application according to your requirement.

To set the **MinDate**, **MaxDate** in your application add the following script in your JSP file.

{% highlight javascript %}

    <script>
    var curdate = new Date(); 
    var rangeDate = new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 30);
    $(function () {
        $("#datepicker").ejDatePicker({
            value: curdate, 
            minDate: curdate,
            maxDate: rangeDate
            });
    });
    </script>

{% endhighlight %}

Run the above code to display the **DatePicker** control with **MinDate** and **MaxDate**.

![JSP DatePicker configuration](Getting Started-images/Datepicker_image2.png) 

