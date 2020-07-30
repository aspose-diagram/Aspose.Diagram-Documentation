---
title : "Get Document Properties" 
description : "" 
weight : 16099 
toc : false
type: docs
url: /net/plugins/vsto/codecomparison/get+document+properties/
---

# Aspose.Diagram for .NET : Get Document Properties


## VSTO

Below is the code to show how to get the diagram document properties:

{{< code lang="cs" >}}
 MessageBox.Show(Application.ActiveDocument.Version.ToString());
 MessageBox.Show(Application.ActiveDocument.BuildNumberCreated.ToString());
 MessageBox.Show(Application.ActiveDocument.BuildNumberEdited.ToString());
 MessageBox.Show(Application.ActiveDocument.TimeCreated.ToString());
 MessageBox.Show(Application.ActiveDocument.TimeEdited.ToString());
 MessageBox.Show(Application.ActiveDocument.TimePrinted.ToString());
 MessageBox.Show(Application.ActiveDocument.TimeSaved.ToString());

{{< /code >}}

## Aspose.Diagram

Below is the code snippet to show how we display the properties of diagram:

{{< code lang="cs" >}}
 //Call the diagram constructor to load diagram from a VDX file
 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Display Visio version and document modification time at different stages
 Console.WriteLine("Visio Instance Version : " + vdxDiagram.Version);
 Console.WriteLine("Full Build Number Created : " + vdxDiagram.DocumentProps.BuildNumberCreated);
 Console.WriteLine("Full Build Number Edited : " + vdxDiagram.DocumentProps.BuildNumberEdited);
 Console.WriteLine("Date Created : " + vdxDiagram.DocumentProps.TimeCreated);
 Console.WriteLine("Date Last Edited : " + vdxDiagram.DocumentProps.TimeEdited);
 Console.WriteLine("Date Last Printed : " + vdxDiagram.DocumentProps.TimePrinted);
 Console.WriteLine("Date Last Saved : " + vdxDiagram.DocumentProps.TimeSaved);
 Console.ReadLine();

{{< /code >}}

## Download Sample Code

*   [Codeplex](https://asposevsto.codeplex.com/releases/view/617141)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932)

## Download Running Code

*   [Codeplex](https://asposevsto.codeplex.com/SourceControl/latest#Aspose.Diagram Vs VSTO Visio/Get Document Properties/)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Get%20Document%20Properties)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932/view/SourceCode#content)

