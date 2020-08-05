---
title : "Retrieve Get Copy and Insert a Page" 
description : "" 
weight : 12026 
toc : false
type: docs
url: /java/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page/
---

# Aspose.Diagram for Java : Retrieve, Get, Copy and Insert a Page


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Retrieving Page Information](#retrieving-page-information)
    *   1.1 [Retrieve Page Information Programming Sample](#retrieve-page-information-programming-sample)
*   2 [Get the Visio Page from a Diagram](#get-the-visio-page-from-a-diagram)
    *   2.1 [Getting a Visio Page Object by ID](#getting-a-visio-page-object-by-id)
        *   2.1.1 [Get Page Object by ID Programming Sample](#get-page-object-by-id-programming-sample)
    *   2.2 [Getting a Visio Page Object by Name](#getting-a-visio-page-object-by-name)
        *   2.2.1 [Get Page Object by Name Programming Sample](#get-page-object-by-name-programming-sample)
*   3 [Copy a Visio Page into Another Diagram](#copy-a-visio-page-into-another-diagram)
    *   3.1 [Copy a Visio Page Programming Sample](#copy-a-visio-page-programming-sample)
*   4 [Copy Visio Page to another Page instance](#copy-visio-page-to-another-page-instance)
*   5 [Insert a Blank Page into a Visio Drawing](#insert-a-blank-page-into-a-visio-drawing)
    *   5.1 [Insert a Blank Page Programming Sample](#insert-a-blank-page-programming-sample)
*   6 [Move Page position in the Visio drawing](#move-page-position-in-the-visio-drawing)
    *   6.1 [Move Page position Programming Sample](#move-page-position-programming-sample)
{{< /panel >}}
 

 

## Retrieving Page Information

In Microsoft Visio, pages are either foreground or background pages. To get page information, for example page ID and page name, first establish whether a page is a background or foreground page.

The [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) object represents the drawing area of a foreground page or a background page. The `Pages` property exposed by the [`Diagram`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/index) class supports a collection of `Aspose.Diagram.Page` objects. This property can be used to retrieve page information.

Use the `Page.Background` property to determine whether a page is a foreground or background page .

The image below shows the output from the code snippets in this article.

**A console showing the output.**  
![image](https://docs2.aspose.com/diagram/java/attachments/18612237/18809119.png)

### Retrieve Page Information Programming Sample

The following piece of code retrieves the pages information from a diagram.

## Get the Visio Page from a Diagram

Sometimes, developers need to get a Visio drawing's page details. Aspose.Diagram has features that helps them do this.

Aspose.Diagram for Java offers the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/index) class that represents a Visio drawing. The `Pages` property exposed by the `Diagram` class supports a collection of `Aspose.Diagram.Page` objects. The `PageCollection` class exposes `GetPage` method that can be called to get `Page` object.

### Getting a Visio Page Object by ID

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Call the `Diagram.Pages` class' `GetPage` method.

The following example shows how to get a page object by id from Visio drawing.

#### Get Page Object by ID Programming Sample

### Getting a Visio Page Object by Name

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Call the `Diagram.Pages` class' `GetPage` method.

#### Get Page Object by Name Programming Sample

The following example shows how to get a page object by name from Visio drawing.

## Copy a Visio Page into Another Diagram

Aspose.Diagram for Java API allows developers to copy and add its content from the one Visio diagram to another. This help topic explains how to accomplish this task.

Aspose.Diagram for Java API has the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/index) class that represents a Visio drawing. The `Pages` property exposed by the `Diagram` class supports a collection of `Aspose.Diagram.Page` objects. The `PageCollection` class exposes `Add` method that can be called to add another `Page` object.

This example work as follows:

1.  Create a new object of the `Diagram` class.
2.  Load an existing Visio diagram into the Diagram class object.
3.  Add all masters from the loaded Visio diagram
4.  Get page object from the loaded diagram (which need to be copied).
5.  Set page object name and id.
6.  Remove empty page of the new diagram (optional).
7.  Call `Add` method of the `PageCollection` class.
8.  Save the new diagram in the computer storage.

### Copy a Visio Page Programming Sample

The code example below shows how to copy a Visio page object into another Visio drawing.

## Copy Visio Page to another Page instance

The Copy method of the Page class takes a page instance to clone.

**Java**

{{< code lang="java" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page newPage = new Page();
// copy page
newPage.copy(diagram.getPages().getPage("Page-1"));
{{< /code >}}

## Insert a Blank Page into a Visio Drawing

[Aspose.Diagram for Java](https://products.aspose.com/diagram/java) can insert a new blank page into the Microsoft Office Visio drawing. This example topic describes how to do so.

The `Add` method, exposed by the `Pages` collection, allows developers to add a new blank page in the Visio diagram. The page ID should be assigned.

### Insert a Blank Page Programming Sample

The following piece of code inserts a blank page in the Visio Drawing:

## Move Page position in the Visio drawing

Aspose.Diagram for Java API can move page position in the Visio drawing. The `moveTo` method, exposed by the `Page` class, helps developers to move the page position.

### Move Page position Programming Sample

The MoveTo member takes the target page index as a parameter to move the position of page in the Visio drawing:

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page newPage = new Page(1);
// move page in the diagram
newPage.moveTo(2);
diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

