+++
title = "Inserting a new Page in Visio" 
description = "" 
weight = 16100 
+++

Aspose.Diagram for .NET : Inserting a new Page in Visio  

# Aspose.Diagram for .NET : Inserting a new Page in Visio


## VSTO

Below is the code to add new page and you can't set the page id that is the drawback we have in MS Visio.

{{< code lang="cs" >}}
 // Add a new blank page
 Application.ActiveDocument.Pages.Add();
 // there is no way to manually set the id of the page in VSTO
{{< /code >}}

## Aspose.Diagram

The `Add` method, exposed by the `Pages` collection, allows you to add a new blank page into a Visio drawing. It must set the page ID.  
Below is the code examples for this:

{{< code lang="cs" >}}
 // Load diagram
 Diagram diagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vsd");

 // Get max page ID
 int MaxPageId = GetMaxPageID(diagram);

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
 diagram.Save(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Output.vdx", SaveFileFormat.VDX);

{{< /code >}}

## Download Sample Code

*   [Codeplex](https://asposevsto.codeplex.com/releases/view/617141)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932)

## Download Running Code

*   [Codeplex](https://asposevsto.codeplex.com/SourceControl/latest#Aspose.Diagram Vs VSTO Visio/Inserting a New Page/)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Inserting%20a%20New%20Page)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932/view/SourceCode#content)

