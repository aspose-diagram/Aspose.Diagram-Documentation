---
title: Få papperets bredd och höjd på sidan
type: docs
weight: 50
url: /sv/net/get-paper-width-and-height-of-page/
description: Det här avsnittet förklarar hur du får pappersstorleken för sidan visio med Aspose.Diagram.
---
## **Möjliga användningsscenarier**

Ibland behöver du veta bredden och höjden på pappersstorleken som den har ställts in i sidinställningarna på sidan. Vänligen använd[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)och[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)fastigheter för detta ändamål.

## **Få sidans bredd och höjd på sidans propellersida**

 Följande exempelkod förklarar användningen av[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)och[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)egenskaper.

### **Exempelkod**


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

