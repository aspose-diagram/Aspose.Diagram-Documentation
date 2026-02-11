---
title: Configuración de márgenes
type: docs
weight: 20
url: /es/net/setting-margins/
description: Esta sección explica cómo configurar las opciones de página de visio con Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram es totalmente compatible con las opciones de configuración de página de Microsoft Visio. Es posible que los desarrolladores necesiten configurar los ajustes de configuración de página para que las páginas controlen el proceso de impresión. Este tema trata sobre cómo usar Aspose.Diagram para configurar los márgenes de página.

{{% /alert %}}

## **Configuración de márgenes**

 Aspose.Diagram proporciona una clase,[**Página**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , que representa un archivo Microsoft Visio. los[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) la clase contiene un[**Paginas**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) colección que permite el acceso a cada página en el archivo Visio. Una página está representada por el[**Página**](https://reference.aspose.com/diagram/net/aspose.diagram/page)clase.

 los[**PáginaHoja**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la clase proporciona la[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) propiedad que se utiliza para establecer las opciones de configuración de página de la página. De hecho, esto[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) La propiedad es un objeto de la[**PáginaHoja**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) clase utilizada para establecer diferentes opciones de diseño de página para una página impresa. los[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class proporciona varias propiedades que se utilizan para establecer las opciones de configuración de la página. Algunas de estas propiedades se analizan a continuación.

### **Márgenes de página**

 Establecer márgenes de página (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) usando[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)miembros de la clase A continuación se enumeran algunos de los métodos que se utilizan para especificar los márgenes de página:

- [**Margen superior de la página**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**Margen inferior de página**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**Margen izquierdo de la página**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**MargenDerechoDePágina**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)

```
{{< highlight "csharp" >}}
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
```