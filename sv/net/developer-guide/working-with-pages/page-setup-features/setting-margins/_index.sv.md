---
title: Ställa in marginaler
type: docs
weight: 20
url: /sv/net/setting-margins/
description: Det här avsnittet förklarar hur du ställer in visios sidalternativ med Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram stöder fullt ut Microsoft Visios sidinställningar. Utvecklare kan behöva konfigurera sidinställningar för sidor för att styra utskriftsprocessen. Det här ämnet diskuterar hur du använder Aspose.Diagram för att konfigurera sidmarginaler.

{{% /alert %}}

## **Ställa in marginaler**

 Aspose.Diagram tillhandahåller en klass,[**Sida**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , som representerar en Microsoft Visio fil. De[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) klass innehåller en[**Sidor**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) samling som ger åtkomst till varje sida i filen Visio. En sida representeras av[**Sida**](https://reference.aspose.com/diagram/net/aspose.diagram/page)klass.

 De[**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) klass ger[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) egenskap som används för att ställa in sidinställningarna för sidan. Faktum är att detta[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) egendom är ett föremål för[**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) klass används för att ställa in olika sidlayoutalternativ för en utskriven sida. De[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class tillhandahåller olika egenskaper som används för att ställa in sidinställningar. Några av dessa egenskaper diskuteras nedan.

### **Sidmarginaler**

 Ställ in sidmarginaler (PageTopMargin, Page BottomMargin, PageLeftMargin, PageRightMargin) med[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)klassmedlemmar. Nedan listas några av metoderna som används för att ange sidmarginaler:

- [**PageTopMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**Page BottomMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set Page Margin
diagram.Pages[0].PageSheet.PrintProps.PageLeftMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageRightMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageTopMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageBottomMargin.Value = 0.01;
{{< /highlight >}}
