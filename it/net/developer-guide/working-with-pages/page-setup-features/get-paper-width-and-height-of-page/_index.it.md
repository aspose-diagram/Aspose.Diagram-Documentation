---
title: Ottieni la larghezza della carta e l'altezza della pagina
type: docs
weight: 50
url: /it/net/get-paper-width-and-height-of-page/
description: Questa sezione spiega come ottenere il formato carta della pagina visio con Aspose.Diagram.
---
## **Possibili scenari di utilizzo**

A volte, è necessario conoscere la larghezza e l'altezza del formato carta poiché è stata impostata nell'impostazione della pagina della pagina. Si prega di utilizzare il[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)e[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)proprietà a questo scopo.

## **Ottieni la larghezza e l'altezza della pagina Prop della pagina**

 Il seguente codice di esempio spiega l'utilizzo di[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)e[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)proprietà.

### **Codice di esempio**


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

