---
title: Lägg till kommentarer till ritningar på Visio
type: docs
weight: 40
url: /sv/net/add-comments-to-drawings-in-visio/
---
## **VSTO**
Nedan är koden för att lägga till kommentarer i diagram:

{{< highlight "cs" >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET låter dig lägga kommentarer var som helst på en diagram-sida.

{{% /alert %}} 

Metoden AddComment, exponerad av klassen Page, låter dig lägga till kommentarer på en ritsida. Den tar X- och Y-koordinaterna tillsammans med en kommentarsträng. Nedan är kodavsnittet:

{{< highlight "cs" >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Ladda ner exempelkod**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Ladda ner Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
