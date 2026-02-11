---
title: Ställa in FitToSheetAcross
type: docs
weight: 10
url: /sv/net/setting-fittosheetacross/
description: Det här avsnittet förklarar hur du ställer in fittosheetacross med Aspose.Diagram.
---
{{% alert color="primary" %}}

Ibland är det nödvändigt att konfigurera sidinställningar för sidor för att styra utskriften. Dessa sidinställningar erbjuder olika alternativ.

{{% /alert %}}

## **Ställa in FitToSheetAcross**

Alternativ för sidinställningar stöds fullt ut i Aspose.Diagram. Den här artikeln förklarar hur du ställer in sidalternativ med Aspose.Diagram och visar kodexempel för inställning:

 Aspose.Diagram tillhandahåller en klass,[**Sida**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , som representerar en Microsoft Visio fil. De[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) klass innehåller en[**Sidor**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) samling som ger åtkomst till varje sida i filen Visio. En sida representeras av[**Sida**](https://reference.aspose.com/diagram/net/aspose.diagram/page)klass.

 De[**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) klass ger[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) egenskap som används för att ställa in sidinställningarna för sidan. Faktum är att detta[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) egendom är ett föremål för[**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) klass används för att ställa in olika sidlayoutalternativ för en utskriven sida. De[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class tillhandahåller olika egenskaper som används för att ställa in sidinställningar. Några av dessa egenskaper diskuteras nedan.

### **FitToSheetAcross**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}
```


