+++
title = "Add Comments to Drawings in Visio" 
description = "" 
weight = 16098 
+++

Aspose.Diagram for .NET : Add Comments to Drawings in Visio  

# Aspose.Diagram for .NET : Add Comments to Drawings in Visio


## VSTO

Below is the code to add comments in diagram:

{{< code lang="cs" >}}
 Page mypage= Application.ActiveDocument.Pages[1];
 mypage.Comments.Add("Test");
{{< /code >}}

## Aspose.Diagram

Aspose.Diagram for .NET allows you to place comments anywhere on a diagram page.

The AddComment method, exposed by the Page class, allows you to add comments to a drawing page. It takes the X and Y coordinates along with a comment string.Below is the code snippet:

{{< code lang="cs" >}}
 // Load diagram
 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment
 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram
 diagram.Save("Output.vdx", SaveFileFormat.VDX);
{{< /code >}}

## Download Sample Code

*   [Codeplex](https://asposevsto.codeplex.com/releases/view/617141)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932)

## Download Running Code

*   [Codeplex](https://asposevsto.codeplex.com/SourceControl/latest#Aspose.Diagram Vs VSTO Visio/Add Comment/)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932/view/SourceCode#content)

