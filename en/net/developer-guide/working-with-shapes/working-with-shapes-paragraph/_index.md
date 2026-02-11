---
title: Working with Shapes Paragraph
type: docs
weight: 40
url: /net/working-with-shapes-paragraph/
---

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Set shape's paragraph.
## **Set shape's Paragraph Programming Sample**
Use the following code in your .NET application to set shape's paragraph using Aspose.Diagram for .NET.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);

// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);

// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);

//Get shape's paragraph
Para para = rectangle.Paras[0];

//Set horizontal of paragraph
para.HorzAlign.Value = HorzAlignValue.LeftAlign;

//Set left indent of paragraph
para.IndLeft.Value = 0.1;

//Set Right indent of paragraph
para.IndRight.Value = 0.1;

//Set First indent of paragraph
para.IndFirst.Value = 0.1;

//Set the amount of space inserted before each paragraph in the shape's text block
para.SpBefore.Value = 0.1;

//Set the amount of space inserted after each paragraph in the shape's text block
para.SpAfter.Value = 0.1;

//Set the distance between one line of text and the next, where 100% is the height of a text line.
para.SpLine.Value = 0.1;

//Set Bullet string of paragraph
para.BulletStr.Value = "";

//Set Bullet string of paragraph
para.Bullet.Value = BulletValue.Style1;

diagram.Save(dataDir + "SettingParagraphOfShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
