+++
title = "Retrieve Get Copy and Insert a Page" 
description = "" 
weight = 12032 
+++

Aspose.Diagram for .NET : Retrieve, Get, Copy and Insert a Page  

# Aspose.Diagram for .NET : Retrieve, Get, Copy and Insert a Page


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Retrieving Page Information](#Retrieve,Get,CopyandInsertaPage-RetrievingPageInformation)
    *   1.1 [Retrieve Page Information Programming Sample](#Retrieve,Get,CopyandInsertaPage-RetrievePageInformationProgrammingSample)
*   2 [Get the Visio Page from a Diagram](#Retrieve,Get,CopyandInsertaPage-GettheVisioPagefromaDiagram)
    *   2.1 [Getting a Visio Page Object by ID](#Retrieve,Get,CopyandInsertaPage-GettingaVisioPageObjectbyID)
        *   2.1.1 [Get Page Object by ID Programming Sample](#Retrieve,Get,CopyandInsertaPage-GetPageObjectbyIDProgrammingSample)
    *   2.2 [Getting a Visio Page Object by Name](#Retrieve,Get,CopyandInsertaPage-GettingaVisioPageObjectbyName)
        *   2.2.1 [Get Page Object by Name Programming Sample](#Retrieve,Get,CopyandInsertaPage-GetPageObjectbyNameProgrammingSample)
*   3 [Copy a Visio Page into Another Diagram](#Retrieve,Get,CopyandInsertaPage-CopyaVisioPageintoAnotherDiagram)
    *   3.1 [Copy a Visio Page Programming Sample](#Retrieve,Get,CopyandInsertaPage-CopyaVisioPageProgrammingSample)
*   4 [Copy Visio Page to another Page instance](#Retrieve,Get,CopyandInsertaPage-CopyVisioPagetoanotherPageinstance)
*   5 [Insert a Blank Page into a Visio Drawing](#Retrieve,Get,CopyandInsertaPage-InsertaBlankPageintoaVisioDrawing)
    *   5.1 [Insert a Blank Page Programming Sample](#Retrieve,Get,CopyandInsertaPage-InsertaBlankPageProgrammingSample)
*   6 [Move Page position in the Visio drawing](#Retrieve,Get,CopyandInsertaPage-MovePagepositionintheVisiodrawing)
    *   6.1 [Move Page position Programming Sample](#Retrieve,Get,CopyandInsertaPage-MovePagepositionProgrammingSample)
{{< /panel >}}
 

 

## Retrieving Page Information

In Microsoft Visio, pages are either foreground or background pages. To get page information, for example page ID and page name, first establish whether a page is a background or foreground page.

The [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The `Pages` property exposed by the [`Diagram`](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supports a collection of `Aspose.Diagram.Page` objects. This property can be used to retrieve page information.

Use the `Page.Background` property to determine whether a page is a foreground or background page .

### Retrieve Page Information Programming Sample

The following piece of code retrieves the pages information from a diagram.

## Get the Visio Page from a Diagram

Sometimes, developers need to get a Visio drawing's page details. Aspose.Diagram has features that helps them do this.

Aspose.Diagram for .NET offers the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The `Pages` property exposed by the `Diagram` class supports a collection of `Aspose.Diagram.Page` objects. The `PageCollection` class exposes `GetPage` method that can be called to get `Page` object.

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

Aspose.Diagram for .NET API allows developers to copy and add its content from the one Visio diagram to another. This help topic explains how to accomplish this task.

Aspose.Diagram for .NET API has the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The `Pages` property exposed by the `Diagram` class supports a collection of `Aspose.Diagram.Page` objects. The `PageCollection` class exposes `Add` method that can be called to add another `Page` object.

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

**C#**

{{< code lang="c#" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page newPage = new Page();
// copy page
newPage.Copy(diagram.Pages.GetPage("Page-1"));
{{< /code >}}

## Insert a Blank Page into a Visio Drawing

[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) can insert a new blank page into the Microsoft Office Visio drawing. This example topic describes how to do so.

The `Add` method, exposed by the `Pages` collection, allows developers to add a new blank page in the Visio diagram. The page ID should be assigned.

### Insert a Blank Page Programming Sample

The following piece of code inserts a blank page in the Visio Drawing:

## Move Page position in the Visio drawing

Aspose.Diagram for .NET API can move page position in the Visio drawing. The `MoveTo` method, exposed by the `Page` class, helps developers to move the page position.

### Move Page position Programming Sample

The MoveTo member takes the target page index as a parameter to move the position of page in the Visio drawing:

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page newPage = new Page(1);
// move page in the diagram
newPage.MoveTo(2);
diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

## Attachments:

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Retrieving page information-001.png](https://docs2.aspose.com/diagram/net/attachments/18350207/18546809.png) (image/png)  

