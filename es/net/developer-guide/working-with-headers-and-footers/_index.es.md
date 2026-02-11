---
title: Trabajar con encabezados y pies de página
type: docs
weight: 140
url: /es/net/working-with-headers-and-footers/
description: Esta sección explica cómo configurar encabezados y pies de página de Microsoft Office Visio con Aspose.Diagram.
---
## **Administrar encabezados y pies de página de los diagramas Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) proporciona un mecanismo para establecer encabezados y pies de página de los diagramas Microsoft Office Visio. Los desarrolladores pueden obtener o establecer la cadena de texto que aparece en el lado izquierdo, central y derecho del encabezado/pie de página de un documento. También pueden establecer el margen del encabezado y pie de página junto con las propiedades de fuente del texto.
### **Configuración de propiedades de encabezados y pies de página**
 los[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)El objeto de clase ofrece la propiedad HeaderFooter que permite obtener y establecer valores de texto, fuente y margen de encabezado y pie de página. Durante la vista previa de impresión del dibujo Visio, los usuarios pueden hacer clic en el botón de enlace "Editar encabezado y pie de página" en Microsoft Visio 2013 (en Microsoft Visio 2010 >> botón "Encabezado y pie de página"). Hay algunas opciones para agregar texto como se muestra en la siguiente captura de pantalla. Los usuarios pueden administrar estas propiedades mediante programación usando Aspose.Diagram API de la siguiente manera:
#### **Ejemplo de programación**
El siguiente fragmento de código ayuda a administrar las propiedades de encabezados y pies de página.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
