---
title: Impostazione di FitToSheetAcross
type: docs
weight: 10
url: /it/net/setting-fittosheetacross/
description: Questa sezione spiega come impostare fittosheetacross con Aspose.Diagram.
---
{{% alert color="primary" %}}

A volte, è necessario configurare le impostazioni di impostazione della pagina per controllare la stampa delle pagine. Queste impostazioni di configurazione della pagina offrono varie opzioni.

{{% /alert %}}

## **Impostazione di FitToSheetAcross**

Le opzioni di impostazione della pagina sono completamente supportate in Aspose.Diagram. Questo articolo spiega come impostare le opzioni della pagina con Aspose.Diagram e mostra esempi di codice per l'impostazione:

 Aspose.Diagram offre un corso,[**Pagina**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , che rappresenta un file Microsoft Visio. Il[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) la classe contiene un[**Pagine**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) raccolta che consente l'accesso a ciascuna pagina del file Visio. Una pagina è rappresentata da[**Pagina**](https://reference.aspose.com/diagram/net/aspose.diagram/page)classe.

 Il[**PaginaFoglio**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la classe fornisce il[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) proprietà utilizzata per impostare le opzioni di impostazione della pagina della pagina. In effetti, questo[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) la proprietà è un oggetto di[**PaginaFoglio**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) classe utilizzata per impostare diverse opzioni di layout di pagina per una pagina stampata. Il[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class fornisce varie proprietà utilizzate per impostare le opzioni di impostazione della pagina. Alcune di queste proprietà sono discusse di seguito.

### **FitToSheetAcross**


{{< highlight csharp >}}
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



