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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageMargin-SetPageMargin.cs" >}}