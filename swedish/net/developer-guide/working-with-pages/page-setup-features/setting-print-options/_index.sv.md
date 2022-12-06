---
title: Ställa in utskriftsalternativ
type: docs
weight: 10
url: /sv/net/setting-print-options/
description: Det här avsnittet förklarar hur du ställer in utskriftsalternativ med Aspose.Diagram.
---
{{% alert color="primary" %}}

Ibland är det nödvändigt att konfigurera sidinställningar för sidor för att styra utskriften. Dessa sidinställningar erbjuder olika alternativ.

{{% /alert %}}

## **Ställa in utskriftsalternativ**

Alternativ för sidinställningar stöds fullt ut i Aspose.Diagram. Den här artikeln förklarar hur du ställer in sidalternativ med Aspose.Diagram och visar kodexempel för inställning:

 Aspose.Diagram tillhandahåller en klass,[**Sida**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , som representerar en Microsoft Visio fil. De[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) klass innehåller en[**Sidor**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) samling som ger åtkomst till varje sida i filen Visio. En sida representeras av[**Sida**](https://reference.aspose.com/diagram/net/aspose.diagram/page)klass.

 De[**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) klass ger[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) egenskap som används för att ställa in sidinställningarna för sidan. Faktum är att detta[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) egendom är ett föremål för[**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) klass används för att ställa in olika sidlayoutalternativ för en utskriven sida. De[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class tillhandahåller olika egenskaper som används för att ställa in sidinställningar. Några av dessa egenskaper diskuteras nedan.

### **Skriv ut Sidorientering**

 Skriv ut Sidorienteringen kan ställas in på stående eller liggande med hjälp av[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) klass'[**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) fast egendom. De[**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) egenskapen accepterar ett av de fördefinierade värdena i[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue)uppräkning, listad nedan.

|**Skriv ut sidorienteringstyper**|**Beskrivning**|
|:- |:- |
|SameAsPrinter|Samma som skrivarens orientering|
|Landskap|Landskapsorientering|
|Porträtt|Stående format|

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageOrientation-SetPageOrientation.cs" >}}

### **Skalningsfaktor**

 Det är möjligt att förminska eller förstora en sidas storlek genom att justera skalfaktorn med[**ScaleX**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex)fast egendom.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageOrientation-SetPageScale.cs" >}}
