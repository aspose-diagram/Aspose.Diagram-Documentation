---
title: Ställa in utskriftsalternativ
type: docs
weight: 10
url: /sv/java/setting-print-options/
description: Det här avsnittet förklarar hur du ställer in utskriftsalternativ med Aspose.Diagram.
---
{{% alert color="primary" %}}

Ibland är det nödvändigt att konfigurera sidinställningar för sidor för att styra utskriften. Dessa sidinställningar erbjuder olika alternativ.

{{% /alert %}}

## **Ställa in utskriftsalternativ**

Alternativ för sidinställningar stöds fullt ut i Aspose.Diagram. Den här artikeln förklarar hur du ställer in sidalternativ med Aspose.Diagram och visar kodexempel för inställning:

 Aspose.Diagram tillhandahåller en klass,[**Sida**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , som representerar en Microsoft Visio fil. De[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass innehåller en[**Sidor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) samling som ger åtkomst till varje sida i filen Visio. En sida representeras av[**Sida**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)klass.

 De[**PageSheet**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) klass ger[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) egenskap som används för att ställa in sidinställningarna för sidan. Faktum är att detta[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) egendom är ett föremål för[**PageSheet**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) klass används för att ställa in olika sidlayoutalternativ för en utskriven sida. De[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)class tillhandahåller olika egenskaper som används för att ställa in sidinställningar. Några av dessa egenskaper diskuteras nedan.

### **Skriv ut Sidorientering**

 Skriv ut Sidorienteringen kan ställas in på stående eller liggande med hjälp av[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) klass'[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) fast egendom. De[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) egenskapen accepterar ett av de fördefinierade värdena i[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)uppräkning, listad nedan.

|**Skriv ut sidorienteringstyper**|**Beskrivning**|
|:- |:- |
|SameAsPrinter|Samma som skrivarens orientering|
|Landskap|Landskapsorientering|
|Porträtt|Stående format|


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);


// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Page page = diagram.getPages().getPage(0);

//Set PrintPageOrientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE);

{{< /highlight >}}


### **Skalningsfaktor**

 Det är möjligt att förminska eller förstora en sidas storlek genom att justera skalfaktorn med[**ScaleX**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)fast egendom.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Page page = diagram.getPages().getPage(0);
//Set ScaleX and ScaleY
page.getPageSheet().getPrintProps().getScaleX().setValue( 1);
page.getPageSheet().getPrintProps().getScaleY().setValue ( 1);
{{< /highlight >}}

