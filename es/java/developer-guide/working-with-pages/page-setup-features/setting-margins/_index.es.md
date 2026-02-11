---
title: Configuración de márgenes
type: docs
weight: 20
url: /es/java/setting-margins/
description: Esta sección explica cómo configurar las opciones de página de visio con Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram es totalmente compatible con las opciones de configuración de página de Microsoft Visio. Es posible que los desarrolladores necesiten configurar los ajustes de configuración de página para que las páginas controlen el proceso de impresión. Este tema trata sobre cómo usar Aspose.Diagram para configurar los márgenes de página.

{{% /alert %}}

## **Configuración de márgenes**

 Aspose.Diagram proporciona una clase,[**Página**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , que representa un archivo Microsoft Visio. los[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) la clase contiene un[**Paginas**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) colección que permite el acceso a cada página en el archivo Visio. Una página está representada por el[**Página**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)clase.

 los[**PáginaHoja**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) la clase proporciona la[**ImprentaAccesorios**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) propiedad que se utiliza para establecer las opciones de configuración de página de la página. De hecho, esto[**ImprentaAccesorios**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) La propiedad es un objeto de la[**PáginaHoja**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) clase utilizada para establecer diferentes opciones de diseño de página para una página impresa. los[**ImprentaAccesorios**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)class proporciona varias propiedades que se utilizan para establecer las opciones de configuración de la página. Algunas de estas propiedades se analizan a continuación.

### **Márgenes de página**

 Establecer márgenes de página (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) usando[**ImprentaAccesorios**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)miembros de la clase A continuación se enumeran algunos de los métodos que se utilizan para especificar los márgenes de página:

- [**Margen superior de la página**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageTopMargin)
- [**Margen inferior de página**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageBottomMargin)
- [**Margen izquierdo de la página**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageLeftMargin)
- [**MargenDerechoDePágina**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageRightMargin)



{{< highlight java >}}
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
