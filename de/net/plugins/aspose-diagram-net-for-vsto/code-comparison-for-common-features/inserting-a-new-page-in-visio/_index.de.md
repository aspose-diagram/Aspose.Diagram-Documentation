---
title: Einfügen einer neuen Seite in Visio
type: docs
weight: 60
url: /de/net/inserting-a-new-page-in-visio/
---
## **VSTO**
Unten ist der Code zum Hinzufügen einer neuen Seite und Sie können die Seiten-ID nicht festlegen, was der Nachteil ist, den wir in MS Visio haben.

{{< highlight "cs" >}}

  // Add a new blank page

 Application.ActiveDocument.Pages.Add();

 // there is no way to manually set the id of the page in VSTO

{{< /highlight >}}
## **Aspose.Diagram**
Die Add-Methode, die von der Pages-Auflistung verfügbar gemacht wird, ermöglicht es Ihnen, eine neue leere Seite in eine Visio-Zeichnung einzufügen. Es muss die Seiten-ID festlegen.
Nachfolgend finden Sie die Codebeispiele dafür:

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
## **Beispielcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Laufcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Inserting%20a%20New%20Page)
