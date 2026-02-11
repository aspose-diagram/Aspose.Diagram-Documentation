---
title: Impostazione dei margini
type: docs
weight: 20
url: /it/net/setting-margins/
description: Questa sezione spiega come impostare le opzioni della pagina di visio con Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram supporta completamente le opzioni di configurazione della pagina di Microsoft Visio. Gli sviluppatori potrebbero dover configurare le impostazioni di configurazione della pagina affinché le pagine controllino il processo di stampa. Questo argomento illustra come utilizzare Aspose.Diagram per configurare i margini della pagina.

{{% /alert %}}

## **Impostazione dei margini**

 Aspose.Diagram offre un corso,[**Pagina**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , che rappresenta un file Microsoft Visio. Il[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) la classe contiene un[**Pagine**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) raccolta che consente l'accesso a ciascuna pagina del file Visio. Una pagina è rappresentata da[**Pagina**](https://reference.aspose.com/diagram/net/aspose.diagram/page)classe.

 Il[**PaginaFoglio**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la classe fornisce il[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) proprietà utilizzata per impostare le opzioni di impostazione della pagina della pagina. In effetti, questo[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) la proprietà è un oggetto di[**PaginaFoglio**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) classe utilizzata per impostare diverse opzioni di layout di pagina per una pagina stampata. Il[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class fornisce varie proprietà utilizzate per impostare le opzioni di impostazione della pagina. Alcune di queste proprietà sono discusse di seguito.

### **Margini della pagina**

 Impostare i margini della pagina (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) utilizzando[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)membri della classe. Di seguito sono elencati alcuni dei metodi utilizzati per specificare i margini della pagina:

- [**PageTopMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
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
