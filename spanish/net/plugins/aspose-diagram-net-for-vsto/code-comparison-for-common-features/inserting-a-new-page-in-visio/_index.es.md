---
title: Insertando una nueva página en Visio
type: docs
weight: 60
url: /es/net/inserting-a-new-page-in-visio/
---
## **VSTO**
continuación se muestra el código para agregar una nueva página y no puede configurar la identificación de la página, ese es el inconveniente que tenemos en MS Visio.

{{< highlight "cs" >}}

  // Add a new blank page

 Application.ActiveDocument.Pages.Add();

 // there is no way to manually set the id of the page in VSTO

{{< /highlight >}}
## **Aspose.Diagram**
El método Agregar, expuesto por la colección Páginas, le permite agregar una nueva página en blanco en un dibujo Visio. Debe establecer el ID de la página.
A continuación se muestran los ejemplos de código para esto:

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
## **Descargar código de muestra**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Descargar código de ejecución**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Inserting%20a%20New%20Page)
