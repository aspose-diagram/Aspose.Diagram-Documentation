---
title: Retrieve, Get, Copy and Insert a Page
type: docs
weight: 10
url: /net/retrieve-get-copy-and-insert-a-page/
description: This section explains how to insert a page, copy a page or get page information with Aspose.Diagram.
---

## **Retrieving Page Information**
In Microsoft Visio, pages are either foreground or background pages. To get page information, for example page ID and page name, first establish whether a page is a background or foreground page.

The [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supports a collection of Aspose.Diagram.Page objects. This property can be used to retrieve page information.

Use the Page.Background property to determine whether a page is a foreground or background page .
### **Retrieve Page Information Programming Sample**
The following piece of code retrieves the pages information from a diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}

## **Get the Visio Page from a Diagram**
Sometimes, developers need to get a Visio drawing's page details. Aspose.Diagram has features that helps them do this.

Aspose.Diagram for .NET offers the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of Aspose.Diagram.Page objects. The PageCollection class exposes GetPage method that can be called to get Page object.
### **Getting a Visio Page Object by ID**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Pages class' GetPage method.

The following example shows how to get a page object by id from Visio drawing.
#### **Get Page Object by ID Programming Sample**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}

### **Getting a Visio Page Object by Name**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Pages class' GetPage method.
#### **Get Page Object by Name Programming Sample**
The following example shows how to get a page object by name from Visio drawing.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}

## **Copy a Visio Page into Another Diagram**
Aspose.Diagram for .NET API allows developers to copy and add its content from the one Visio diagram to another. This help topic explains how to accomplish this task.

Aspose.Diagram for .NET API has the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of Aspose.Diagram.Page objects. The PageCollection class exposes Add method that can be called to add another Page object.

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Copy Visio Page to another Page instance**
The Copy method of the Page class takes a page instance to clone.

**C#**

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Insert a Blank Page into a Visio Drawing**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) can insert a new blank page into the Microsoft Office Visio drawing. This example topic describes how to do so.

The Add method, exposed by the Pages collection, allows developers to add a new blank page in the Visio diagram. The page ID should be assigned.
### **Insert a Blank Page Programming Sample**
The following piece of code inserts a blank page in the Visio Drawing:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Move Page position in the Visio drawing**
Aspose.Diagram for .NET API can move page position in the Visio drawing. The MoveTo method, exposed by the Page class, helps developers to move the page position.
### **Move Page position Programming Sample**
The MoveTo member takes the target page index as a parameter to move the position of page in the Visio drawing:

{{< highlight java >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
