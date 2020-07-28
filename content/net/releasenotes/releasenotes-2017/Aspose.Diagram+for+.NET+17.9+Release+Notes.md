+++
title = "Aspose.Diagram for .NET 17.9 Release Notes" 
description = "" 
weight = 12146 
+++

Aspose.Diagram for .NET : Aspose.Diagram for .NET 17.9 Release Notes  

# Aspose.Diagram for .NET : Aspose.Diagram for .NET 17.9 Release Notes


This page contains release notes for [Aspose.Diagram for .NET 17.9](https://www.nuget.org/packages/Aspose.Diagram/17.9.0).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMNET-51261|Add support of converting the specific area of a drawing to image|Enhancement|
|DIAGRAMNET-51350|Add support to retrieve shape by name|Enhancement|
|DIAGRAMNET-51351|Add support of retrieving the shape from Annotation|Enhancement|
|DIAGRAMNET-51295|VSDX to SVG - the low quality of output SVG|Bug|
|DIAGRAMNET-51309|DiagramException occurs on VSDX file saving|Bug|
|DIAGRAMNET-51331|VSDM to SVG - the text items are shifted up|Bug|
|DIAGRAMNET-51333|VSDM to SVG - incorrect rendering of the circular icons|Bug|
|DIAGRAMNET-51339|VSDX to SVG - the truncation of text from the right side of each image|Bug|
|DIAGRAMNET-51340|Incorrect comments order|Bug|
| DIAGRAMNET-51342|Out of memory error after using the "AddComment" method and save file to steam|Bug|
|DIAGRAMNET-51344|VSDX to PDF - an argument out of range error occurred|Bug|
|DIAGRAMNET-51345|The comment is not deleted together with the shape|Bug|
|DIAGRAMNET-51346|VSDM to SVG - the logo quality is downgraded|Bug|
|DIAGRAMNET-51347|VSDM to SVG - the logo quality is downgraded|Bug|
|DIAGRAMNET-51353|Cannot add another comment in the Visio page|Bug|
|DIAGRAMNET-51354|Cannot edit comments in the Visio page|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).

### Adds GetShape member in ShapeCollection 

It allows to retrieve a shape by name.

string dataDir = @"C:\\temp\\";// load a drawingDiagram diagram = new Diagram(dataDir + "Drawing1.vsdx");// retrieve page by namePage page = diagram.Pages.GetPage("Page-1");// retrieve shape by nameShape shape = page.Shapes.GetShape("name");

### Adds ShapeID member in Annotation

It allows to track the shape of comment.

string dataDir = @"C:\\temp\\";// load a drawingDiagram diagram = new Diagram(dataDir + "Drawing1.vsdx");// get the annotation by indexAnnotation annotation = diagram.Pages.GetPage("Page-1").PageSheet.Annotations\[1\];// get shape IdConsole.WriteLine(annotation.ShapeID);

### Adds Area in RenderingSaveOptions

It allows to convert the specific rectangle region of Visio drawing.

// load a Visio drawingDiagram diagram = new Diagram(@"c:\\\\test.vsdx");ImageSaveOptions Options = new ImageSaveOptions(SaveFileFormat.PNG);// specify regionOptions.Area = new RectangleF(0, 0, 1, 1);// save into the image formatdiagram.Save("e:\\\\area.png", Options);

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs: 

1.  [Convert Specified Area of the Visio Page to an Image](https://docs2.aspose.com/diagram/net/developerguide/working+with+images#workingwithimages-convertspecifiedareaofthevisiopagetoanimage)
2.  [Auto-space a Collection of Shapes in the Visio Page](https://docs2.aspose.com/diagram/net/developerguide/workingwithpages/auto-space+a+collection+of+shapes+in+the+visio+page)

