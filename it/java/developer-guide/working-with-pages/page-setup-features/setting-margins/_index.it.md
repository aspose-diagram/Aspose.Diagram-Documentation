---
title: Impostazione dei margini
type: docs
weight: 20
url: /it/java/setting-margins/
description: Questa sezione spiega come impostare le opzioni della pagina di visio con Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram supporta completamente le opzioni di configurazione della pagina di Microsoft Visio. Gli sviluppatori potrebbero dover configurare le impostazioni di configurazione della pagina affinché le pagine controllino il processo di stampa. Questo argomento illustra come utilizzare Aspose.Diagram per configurare i margini della pagina.

{{% /alert %}}

## **Impostazione dei margini**

 Aspose.Diagram offre un corso,[**Pagina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , che rappresenta un file Microsoft Visio. Il[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) la classe contiene un[**Pagine**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) raccolta che consente l'accesso a ciascuna pagina del file Visio. Una pagina è rappresentata da[**Pagina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)classe.

 Il[**PaginaFoglio**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) la classe fornisce il[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) proprietà utilizzata per impostare le opzioni di impostazione della pagina della pagina. In effetti, questo[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) la proprietà è un oggetto di[**PaginaFoglio**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) classe utilizzata per impostare diverse opzioni di layout di pagina per una pagina stampata. Il[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)class fornisce varie proprietà utilizzate per impostare le opzioni di impostazione della pagina. Alcune di queste proprietà sono discusse di seguito.

### **Margini della pagina**

 Impostare i margini della pagina (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) utilizzando[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)membri della classe. Di seguito sono elencati alcuni dei metodi utilizzati per specificare i margini della pagina:

- [**PageTopMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageTopMargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageBottomMargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageLeftMargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageRightMargin)


```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set Page Margin
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageLeftMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageRightMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageTopMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageBottomMargin().setValue( 0.01);
{{< /highlight >}}
```