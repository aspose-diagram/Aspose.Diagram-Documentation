---
title: Impostazione delle opzioni di stampa
type: docs
weight: 10
url: /it/java/setting-print-options/
description: Questa sezione spiega come impostare le opzioni di stampa con Aspose.Diagram.
---
{{% alert color="primary" %}}

A volte, è necessario configurare le impostazioni di impostazione della pagina per controllare la stampa delle pagine. Queste impostazioni di configurazione della pagina offrono varie opzioni.

{{% /alert %}}

## **Impostazione delle opzioni di stampa**

Le opzioni di impostazione della pagina sono completamente supportate in Aspose.Diagram. Questo articolo spiega come impostare le opzioni della pagina con Aspose.Diagram e mostra esempi di codice per l'impostazione:

 Aspose.Diagram offre un corso,[**Pagina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , che rappresenta un file Microsoft Visio. Il[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) la classe contiene un[**Pagine**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) raccolta che consente l'accesso a ciascuna pagina del file Visio. Una pagina è rappresentata da[**Pagina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)classe.

 Il[**PaginaFoglio**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) la classe fornisce il[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) proprietà utilizzata per impostare le opzioni di impostazione della pagina della pagina. In effetti, questo[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) la proprietà è un oggetto di[**PaginaFoglio**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) classe utilizzata per impostare diverse opzioni di layout di pagina per una pagina stampata. Il[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)class fornisce varie proprietà utilizzate per impostare le opzioni di impostazione della pagina. Alcune di queste proprietà sono discusse di seguito.

### **Stampa orientamento pagina**

 Stampa L'orientamento della pagina può essere impostato su verticale o orizzontale utilizzando il[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) classe'[**StampaOrientamentoPagina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) proprietà. Il[**StampaOrientamentoPagina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) La proprietà accetta uno dei valori predefiniti in[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)enumerazione, di seguito elencati.

|**Stampa i tipi di orientamento della pagina**|**Descrizione**|
|:- |:- |
|Uguale alla stampante|Uguale all'orientamento della stampante|
|Paesaggio|Orientamento orizzontale|
|Ritratto|Orientamento verticale|


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


### **Fattore di scala**

 È possibile ridurre o ingrandire le dimensioni di una pagina regolando il fattore di scala con il[**ScalaX**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)proprietà.


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

