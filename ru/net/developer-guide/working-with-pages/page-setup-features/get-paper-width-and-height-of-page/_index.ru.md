---
title: Получить ширину бумаги и высоту страницы
type: docs
weight: 50
url: /ru/net/get-paper-width-and-height-of-page/
description: В этом разделе объясняется, как получить размер бумаги страницы visio с помощью Aspose.Diagram.
---
## **Возможные сценарии использования**

Иногда вам нужно знать ширину и высоту размера бумаги, поскольку они были установлены в настройках страницы. Пожалуйста, используйте[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)а также[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)свойств для этой цели.

## **Получить ширину страницы и высоту страницы Опора страницы**

 В следующем примере кода объясняется использование[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)а также[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)характеристики.

### **Образец кода**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");

// Get page's width and height
double pagewidth = page.PageSheet.PageProps.PageWidth.Value;
double pageheight = page.PageSheet.PageProps.PageHeight.Value;

{{< /highlight >}}

