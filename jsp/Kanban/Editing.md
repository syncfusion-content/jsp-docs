---
layout: post
title:  Editing
description: Editing
documentation: ug
platform: jsp
keywords: editing,kanban editing
---

# Editing

The Kanban control has support for dynamic insertion, updating and deletion of cards. 

Set `allowEditing` and `allowAdding` property as true to enable editing/inserting respectively. The primary key for the data source should be defined in `primaryKey`, for editing to work properly. 

You can start the edit action by double clicking the particular card. Similarly, you can add new card to Kanban either by double clicking the particular cell or on an external button which is bound to call `addCard` method of Kanban. 

Deletion of the card is possible by using [`deleteCard`](https://help.syncfusion.com/api/js/ejkanban#methods:kanbanedit-deletecard) by passing primary key as attribute.

N> In Kanban, the `primary key` column will be automatically set to `read only` while editing the card which is to avoid duplicate entry in the cards.

## Configuring Edit Items

You need to configure the list of data source fields that are allowable in editing state using `editItems` property. The `field` property of `editItems` needs to be mapped with data source fields.

You can map the data source field as title to edit form using `title` property of `fields`. By default, it’s mapped with `primaryKey`.

The following code example describes the above behavior.

{% highlight html %}

    <%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%><%@ taglib prefix="ej" uri="/WEB-INF/EJ.tld" %><%@ page import="com.syncfusion.*" %><%@ page session="false" import="java.util.ArrayList" %><%@ page session="false" import="java.util.Iterator" %><%@ page session="false" import="org.json.simple.parser.JSONParser" %><%@ page import="datasource.GetJsonData" %>
    <script type="text/javascript" src="Scripts/jquery.validate.min.js"></script>
    <script type="text/javascript" src="Scripts/jquery.validate.unobtrusive.min.js"></script>
    <body>
	<div class="cols-sample-area"><%
    GetJsonData obj=new GetJsonData();
    Object data = obj.GetKanbanJson();
    JSONParser parser = new JSONParser();
    request.setAttribute("KanbanDataSource",data);
	request.setAttribute("StringValidation",parser.parse("{\"required\": true,\"number\":true}"));
	request.setAttribute("GetNumericParam",parser.parse("{\"decimalPlaces\":2}"));
    %>
		<ej:kanban id="Kanban" keyField="Status" dataSource="${KanbanDataSource}">
			<ej:kanban-fields content="Summary" primaryKey="Id"></ej:kanban-fields>
			<ej:kanban-columns>
				<ej:kanban-column headerText="Backlog" key="Open"></ej:kanban-column>
				<ej:kanban-column headerText="In Progress" key="InProgress"></ej:kanban-column>
				<ej:kanban-column headerText="Done" key="Close"></ej:kanban-column>
			</ej:kanban-columns>
			<ej:kanban-editSettings allowAdding="true" allowEditing="true">
				<ej:kanban-editSettings-editItems>
					<ej:kanban-editSettings-editItem field="Id"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Status" editType="dropdownedit"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Assignee" editType="dropdownedit"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Estimate" editType="numericedit"  editParams="${GetNumericParam}"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Summary" editType="textarea" ></ej:kanban-editSettings-editItem>
				</ej:kanban-editSettings-editItems>
			</ej:kanban-editSettings>
		</ej:kanban>
	</div>
    </body>
    </html>

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Editing_images/editing_img1.png)

## Edit modes

### Dialog

Set `editMode` as `dialog` to edit data using a dialog box, which displays the fields associated with the data card being edited. Default value is `dialog`.

N> For `editMode` property you can assign either `string` value (“dialog”) or `enum` value (`ej.Kanban.EditMode.Dialog`).

The following code example describes the above behavior.

{% highlight html %}

    <%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%><%@ taglib prefix="ej" uri="/WEB-INF/EJ.tld" %><%@ page import="com.syncfusion.*" %><%@ page session="false" import="java.util.ArrayList" %><%@ page session="false" import="java.util.Iterator" %><%@ page session="false" import="org.json.simple.parser.JSONParser" %><%@ page import="datasource.GetJsonData" %>
    <script type="text/javascript" src="Scripts/jquery.validate.min.js"></script>
    <script type="text/javascript" src="Scripts/jquery.validate.unobtrusive.min.js"></script>
    <body>
	<div class="cols-sample-area"><%
    GetJsonData obj=new GetJsonData();
    Object data = obj.GetKanbanJson();
    JSONParser parser = new JSONParser();
    request.setAttribute("KanbanDataSource",data);
	request.setAttribute("StringValidation",parser.parse("{\"required\": true,\"number\":true}"));
	request.setAttribute("GetNumericParam",parser.parse("{\"decimalPlaces\":2}"));
    %>
		<ej:kanban id="Kanban" keyField="Status" dataSource="${KanbanDataSource}">
			<ej:kanban-fields content="Summary" primaryKey="Id"></ej:kanban-fields>
			<ej:kanban-columns>
				<ej:kanban-column headerText="Backlog" key="Open"></ej:kanban-column>
				<ej:kanban-column headerText="In Progress" key="InProgress"></ej:kanban-column>
				<ej:kanban-column headerText="Done" key="Close"></ej:kanban-column>
			</ej:kanban-columns>
			<ej:kanban-editSettings allowAdding="true" allowEditing="true">
				<ej:kanban-editSettings-editItems>
					<ej:kanban-editSettings-editItem field="Id"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Status" editType="dropdownedit"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Assignee" editType="dropdownedit"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Estimate" editType="numericedit"  editParams="${GetNumericParam}"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Summary" editType="textarea" ></ej:kanban-editSettings-editItem>
				</ej:kanban-editSettings-editItems>
			</ej:kanban-editSettings>
		</ej:kanban>
	</div>
    </body>
    </html>

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Editing_images/editing_img2.png)

## Column Validation

We can validate the value of the added or edited card cell before saving.

The below validation script files are needed when editing is enabled with validation.

1.	jquery.validate.min.js
2.	jquery.validate.unobtrusive.min.js

N> If you enabled the unobtrusive option, then need to refer the jquery.validate.unobtrusive.min.js
file in your application along with the other script.

### jQuery Validation

You can set validation rules using `validationRules` property of `columns`. The following are jQuery validation methods.

#### List of jQuery validation methods

<table>
<tr>
<th>
Rules</th><th>
Description</th>
</tr>
<tr>
<td>
required</td><td>
Requires an element.</td></tr>
<tr>
<td>
remote</td><td>
Requests a resource to check the element for validity.</td></tr>
<tr>
<td>
minlength</td><td>
Requires the element to be of given minimum length.</td></tr>
<tr>
<td>
maxlength</td><td>
Requires the element to be of given maximum length.</td></tr>
<tr>
<td>
rangelength</td><td>
Requires the element to be in given value range.</td></tr>
<tr>
<td>
min</td><td>
The element requires a given minimum.</td></tr>
<tr>
<td>
max</td><td>
The element requires a given maximum.</td></tr>
<tr>
<td>
range</td><td>
Requires the element to be in a given value range.</td></tr>
<tr>
<td>
email</td><td>
The element requires a valid email.</td></tr>
<tr>
<td>
url</td><td>
The element requires a valid url.</td></tr>
<tr>
<td>
date</td><td>
Requires the element to be a date.</td></tr>
<tr>
<td>
dateISO</td><td>
The element requires an ISO date.</td></tr>
<tr>
<td>
number</td><td>
The element requires a decimal number.</td></tr>
<tr>
<td>
digits</td><td>
The element requires digits only.</td></tr>
<tr>
<td>
creditcard</td><td>
Requires the element to be a credit card number.</td></tr>
<tr>
<td>
equalTo</td><td>
Requires the element to be the same as another.</td></tr>
</table>

Kanban supports all the standard validation methods of jQuery, please refer the jQuery validation documentation [`link`](https://jqueryvalidation.org/) for more information.

The following code example describes the above behavior.

{% highlight html %}

    <%@ page language="java" contentType="text/html; charset=ISO-8859-1"
    pageEncoding="ISO-8859-1"%><%@ taglib prefix="ej" uri="/WEB-INF/EJ.tld" %><%@ page import="com.syncfusion.*" %><%@ page session="false" import="java.util.ArrayList" %><%@ page session="false" import="java.util.Iterator" %><%@ page session="false" import="org.json.simple.parser.JSONParser" %><%@ page import="datasource.GetJsonData" %>
    <script type="text/javascript" src="Scripts/jquery.validate.min.js"></script>
    <script type="text/javascript" src="Scripts/jquery.validate.unobtrusive.min.js"></script>
    <body>
	<div class="cols-sample-area"><%
    GetJsonData obj=new GetJsonData();
    Object data = obj.GetKanbanJson();
    JSONParser parser = new JSONParser();
    request.setAttribute("KanbanDataSource",data);
	request.setAttribute("StringValidation",parser.parse("{\"required\": true,\"number\":true}"));
	request.setAttribute("GetNumericParam",parser.parse("{\"decimalPlaces\":2}"));
	request.setAttribute("Estimatevalidation",parser.parse("{\"range\": [0, 1000] }"));
	request.setAttribute("TextareaValdation",parser.parse("{\"required\": \"true\"}"));
    %>
		<ej:kanban id="Kanban" keyField="Status" allowTitle="true" allowSelection="true" dataSource="${KanbanDataSource}">
			<ej:kanban-fields content="Summary" primaryKey="Id" imageUrl="ImgUrl"></ej:kanban-fields>
			<ej:kanban-columns>
				<ej:kanban-column headerText="Backlog" key="Open"></ej:kanban-column>
				<ej:kanban-column headerText="In Progress" key="InProgress"></ej:kanban-column>
				<ej:kanban-column headerText="Testing" key="Testing"></ej:kanban-column>
				<ej:kanban-column headerText="Done" key="Close"></ej:kanban-column>
			</ej:kanban-columns>
			<ej:kanban-editSettings allowAdding="true" allowEditing="true">
				<ej:kanban-editSettings-editItems>
					<ej:kanban-editSettings-editItem field="Id" editType="stringedit" validationRules="${StringValidation}"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Status" editType="dropdownedit"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Assignee" editType="dropdownedit"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Estimate" editType="numericedit"  editParams="${GetNumericParam}" validationRules="${Estimatevalidation}"></ej:kanban-editSettings-editItem>
					<ej:kanban-editSettings-editItem field="Summary" editType="textarea" validationRules="${TextareaValdation}"></ej:kanban-editSettings-editItem>
				</ej:kanban-editSettings-editItems>
			</ej:kanban-editSettings>
		</ej:kanban>
	</div>
    </body>
    </html>

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Editing_images/editing_img5.png)

