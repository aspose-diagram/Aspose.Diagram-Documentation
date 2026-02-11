---
title: Working with Headers and Footers
type: docs
weight: 140
url: /net/working-with-headers-and-footers/
description: This section explains how to set headers and footers of the Microsoft Office Visio with Aspose.Diagram.
---

## **Manage Headers and Footers of the Visio Diagrams**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) provides a mechanism for setting headers and footers of the Microsoft Office Visio diagrams. Developers can get or set the text string that appears on the left, center and right side of a document header/footer. They can also set header and footer margin along with the font properties of the text.
### **Setting Headers and Footers Properties**
The [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class object offers HeaderFooter property which allows to get and set header and footer text, font and margin values. During the print preview of Visio drawing, users can click on "Edit Header & Footer" link button in Microsoft Visio 2013 (in Microsoft Visio 2010 >> "Header & Footer" button). There are a few options to add text as shown in the screenshot below. Users can manage these properties programmatically using Aspose.Diagram API as follows:
#### **Programming Sample**
The following piece of code helps to manage Headers and Footers properties.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

