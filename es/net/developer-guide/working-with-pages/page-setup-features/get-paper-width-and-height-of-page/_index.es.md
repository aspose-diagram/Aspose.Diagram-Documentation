---
title: Obtenga el ancho del papel y la altura de la página
type: docs
weight: 50
url: /es/net/get-paper-width-and-height-of-page/
description: Esta sección explica cómo obtener el tamaño de papel de la página visio con Aspose.Diagram.
---
## **Posibles escenarios de uso**

A veces, necesita saber el ancho y la altura del tamaño del papel tal como se configuró en la configuración de página de la página. Por favor use el[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)y[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)propiedades para este fin.

## **Obtener el ancho y el alto de la página Prop de la página**

 El siguiente código de ejemplo explica el uso de[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)y[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)propiedades.

### **Código de muestra**

```
{{< highlight "csharp" >}}
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
```
