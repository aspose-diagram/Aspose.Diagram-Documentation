---
title: Writing Document Summary
type: docs
weight: 70
url: /net/writing-document-summary/
---

## **VSTO**
Below is the code for writing document summary of Visio:

{{< highlight cs >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio lets you define a number of document summary information properties to help you and your colleagues identify a diagram. Summary properties, for example title, subject, author and description, makes the file easier to find when searching, and easier to recognize when browsing files.

{{% /alert %}} 
### **Writing Microsoft Visio Document Summary Info**
The [DocumentProperties](/pages/createpage.action?spaceKey=diagramnet&title=DocumentProperties+Class&linkCreation=true&fromPageId=18354908) class exposes a number of properties to set or get a Microsoft Visio diagram's summary information. Aspose.Diagram for .NET can update the drawing summary information and then write the drawing file back to VDX.

To update the drawing summary information of an existing VDX or VSD file:

1. Create an instance of the [Diagram](/pages/createpage.action?spaceKey=diagramnet&title=Diagram+Class&linkCreation=true&fromPageId=18354908) class.
1. Set properties exposed by Diagram.DocumentProps to define the summary information for the Visio drawing file.
1. Call the Diagram class' Save method to write the Visio drawing file to VDX.

Check the summary information:

1. Open the output VDX file in Microsoft Visio.
1. Selecting **Info** from the **File** menu.

{{< highlight cs >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Download Sample Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Download Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
