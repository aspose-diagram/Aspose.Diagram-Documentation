---
title: Вставка новой страницы в Visio
type: docs
weight: 60
url: /ru/net/inserting-a-new-page-in-visio/
---
## **ВСТО**
Ниже приведен код для добавления новой страницы, и вы не можете установить идентификатор страницы, что является недостатком, который мы имеем в MS Visio.

{{< highlight "cs" >}}

  // Add a new blank page

 Application.ActiveDocument.Pages.Add();

 // there is no way to manually set the id of the page in VSTO

{{< /highlight >}}
## **Aspose.Diagram**
Метод Add, предоставляемый коллекцией Pages, позволяет добавить новую пустую страницу в рисунок Visio. Он должен установить идентификатор страницы.
Ниже приведены примеры кода для этого:

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
## **Скачать пример кода**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Скачать рабочий код**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Inserting%20a%20New%20Page)
