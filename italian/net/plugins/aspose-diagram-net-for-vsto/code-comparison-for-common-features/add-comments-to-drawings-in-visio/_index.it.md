---
title: Aggiungi commenti ai disegni in Visio
type: docs
weight: 40
url: /it/net/add-comments-to-drawings-in-visio/
---
## **VSTO**
Di seguito è riportato il codice per aggiungere commenti in diagram:

{{< highlight "cs" >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET consente di inserire commenti ovunque su una pagina diagram.

{{% /alert %}} 

Il metodo AddComment, esposto dalla classe Page, consente di aggiungere commenti a una pagina di disegno. Prende le coordinate X e Y insieme a una stringa di commento. Di seguito è riportato il frammento di codice:

{{< highlight "cs" >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Scarica il codice di esempio**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Scarica il codice in esecuzione**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
