---
layout: post
title: Getting started with JSP RadioButton | Syncfusion
description: Learn here about getting started with Syncfusion Essential JSP RadioButton control, its elements, and more. 
platform: JSP
control: RadioButton
documentation: ug
---

# GettingStarted with JSP RadioButton

This section briefly describes about how to create a **RadioButton** in your application with JSP.

## Create a simple RadioButton in JSP

You can create an JSP application and add necessary scripts with the help of the given [JSP Getting Started Documentation.](/jsp-docs/jsp/Getting-Started)

Create the JSP file and add the below given code to render **RadioButton** control.

{% highlight javascript %}

<div>
     Category<br> <br>
     <table>
        <tr>
            <td>
                <ej:radioButton id="radio1" name="Category" size="small" value="fresher"></ej:radioButton>
                <label for="radio1">Fresher</label>
            </td>
            <td colspan="2">
                <ej:radioButton id="radio2" name="Category" size="small" value="experienced" checked="true"></ej:radioButton>
                <label for="radio2">Experienced</label>
            </td>
        </tr>
     </table><br>
     Experience <br>
     <table>
        <tr>
            <td>
                <ej:radioButton id="radio3" name="experienced" size="medium" value="1+years" checked="true"></ej:radioButton>
                <label for="radio3">1+ Years</label>
            </td>
            <td colspan="2">
                <ej:radioButton id="radio4" name="experienced" size="medium" value="2.5+ Years"></ej:radioButton>
                <label for="radio4">2.5+ Years</label>
            </td>
            <td colspan="2">
                <ej:radioButton id="radio5" name="experienced" size="medium" value="5+ years"></ej:radioButton>
                <label for="radio5">5+ Years</label>
            </td>
        </tr>
     </table>
</div>

{% endhighlight %}

You can execute the above code example to display the **RadioButton** control .

![JSP RadioButton Getting Started](getting-started_images/radiobutton.png) 
