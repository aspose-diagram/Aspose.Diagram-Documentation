---
title: Retrieve, Get, Copy and Insert a Page
type: docs
weight: 10
url: /java/retrieve-get-copy-and-insert-a-page/
---

## **Retrieving Page Information**
In Microsoft Visio, pages are either foreground or background pages. To get page information, for example page ID and page name, first establish whether a page is a background or foreground page.

The [Page](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](https://apireference.aspose.com/diagram/java) class supports a collection of Aspose.Diagram.Page objects. This property can be used to retrieve page information.

Use the Page.Background property to determine whether a page is a foreground or background page .

The image below shows the output from the code snippets in this article.

**A console showing the output.** 

![todo:image_alt_text](retrieve-get-copy-and-insert-a-page_1.png)
### **Retrieve Page Information Programming Sample**
The following piece of code retrieves the pages information from a diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-RetrievePageInfo-RetrievePageInfo.java" >}}
## **Get the Visio Page from a Diagram**
Sometimes, developers need to get a Visio drawing's page details. Aspose.Diagram has features that helps them do this.

Aspose.Diagram for Java offers the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of Aspose.Diagram.Page objects. The PageCollection class exposes GetPage method that can be called to get Page object.
### **Getting a Visio Page Object by ID**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Pages class' GetPage method.

The following example shows how to get a page object by id from Visio drawing.
#### **Get Page Object by ID Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyID-GetVisioPagebyID.java" >}}
### **Getting a Visio Page Object by Name**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Pages class' GetPage method.
#### **Get Page Object by Name Programming Sample**
The following example shows how to get a page object by name from Visio drawing.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyName-GetVisioPagebyName.java" >}}
## **Copy a Visio Page into Another Diagram**
Aspose.Diagram for Java API allows developers to copy and add its content from the one Visio diagram to another. This help topic explains how to accomplish this task.

Aspose.Diagram for Java API has the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of Aspose.Diagram.Page objects. The PageCollection class exposes Add method that can be called to add another Page object.

This example work as follows:

1. Create a new object of the Diagram class.
1. Load an existing Visio diagram into the Diagram class object.
1. Add all masters from the loaded Visio diagram
1. Get page object from the loaded diagram (which need to be copied).
1. Set page object name and id.
1. Remove empty page of the new diagram (optional).
1. Call Add method of the PageCollection class.
1. Save the new diagram in the computer storage.
### **Copy a Visio Page Programming Sample**
The code example below shows how to copy a Visio page object into another Visio drawing.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-CopyVisioPage-CopyVisioPage.java" >}}
## **Copy Visio Page to another Page instance**
The Copy method of the Page class takes a page instance to clone.

**Java**

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Insert a Blank Page into a Visio Drawing**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) can insert a new blank page into the Microsoft Office Visio drawing. This example topic describes how to do so.

The Add method, exposed by the Pages collection, allows developers to add a new blank page in the Visio diagram. The page ID should be assigned.
### **Insert a Blank Page Programming Sample**
The following piece of code inserts a blank page in the Visio Drawing:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.java" >}}
## **Move Page position in the Visio drawing**
Aspose.Diagram for Java API can move page position in the Visio drawing. The moveTo method, exposed by the Page class, helps developers to move the page position.
### **Move Page position Programming Sample**
The MoveTo member takes the target page index as a parameter to move the position of page in the Visio drawing:

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
