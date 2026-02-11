---
title: Ta bort dold information
type: docs
weight: 50
url: /sv/net/remove-hidden-info/
description: Det här avsnittet förklarar hur man tar bort oanvändbar eller dold information från en diagram med Aspose.Diagram.
---
## **Ta bort dold information**
 Aspose.Diagram for .NET API tillåter utvecklare att ta bort dold information från en diagram. För att ta bort dold information kan du använda**RemoveHiddenInfoItem** fastigheter i**RemoveHiddenInformation()**metod av Diagram klass. Kodexemplet nedan visar hur man ritar ta bort dold info från diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();
// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Remove hidden information from diagram
diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));
// Initialize HTML save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Save the Visio diagram
diagram.Save(dataDir + "RemoveHiddenInfo_out.html", options);

{{< /highlight >}}

