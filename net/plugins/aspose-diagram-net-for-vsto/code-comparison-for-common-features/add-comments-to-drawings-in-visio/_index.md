---
title: Add Comments to Drawings in Visio
type: docs
weight: 40
url: /net/add-comments-to-drawings-in-visio/
---

## **VSTO**
Below is the code to add comments in diagram:

{{< highlight cs >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET allows you to place comments anywhere on a diagram page.

{{% /alert %}} 

The AddComment method, exposed by the Page class, allows you to add comments to a drawing page. It takes the X and Y coordinates along with a comment string.Below is the code snippet:

{{< highlight cs >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Download Sample Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Download Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
