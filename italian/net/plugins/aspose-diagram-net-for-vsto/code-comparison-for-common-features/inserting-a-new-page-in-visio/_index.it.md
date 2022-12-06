---
title: Inserimento di una nuova Pagina in Visio
type: docs
weight: 60
url: /it/net/inserting-a-new-page-in-visio/
---
## **VSTO**
Di seguito è riportato il codice per aggiungere una nuova pagina e non è possibile impostare l'ID della pagina che è lo svantaggio che abbiamo in MS Visio.

{{< highlight "cs" >}}

  // Add a new blank page

 Application.ActiveDocument.Pages.Add();

 // there is no way to manually set the id of the page in VSTO

{{< /highlight >}}
## **Aspose.Diagram**
Il metodo Add, esposto dalla raccolta Pages, consente di aggiungere una nuova pagina vuota in un disegno Visio. Deve impostare l'ID della pagina.
Di seguito sono riportati gli esempi di codice per questo:

{{< highlight "cs" >}}

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


{{< /highlight >}}
## **Scarica il codice di esempio**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Scarica il codice in esecuzione**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Inserting%20a%20New%20Page)
