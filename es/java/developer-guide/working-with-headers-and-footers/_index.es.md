---
title: Trabajar con encabezados y pies de página
type: docs
weight: 150
url: /es/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java proporciona un mecanismo para establecer encabezados y pies de página de los diagramas Microsoft Office Visio. Los desarrolladores pueden obtener o establecer la cadena de texto que aparece en el lado izquierdo, central y derecho del encabezado/pie de página de un documento. También pueden establecer el margen del encabezado y pie de página junto con las propiedades de fuente del texto.

{{% /alert %}} 
### **Configuración de propiedades de encabezados y pies de página**
 los[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)El objeto de clase ofrece la propiedad HeaderFooter que permite obtener y establecer valores de texto, fuente y margen de encabezado y pie de página. Durante la vista previa de impresión del dibujo Visio, los usuarios pueden hacer clic en el botón de enlace "Editar encabezado y pie de página" en Microsoft Visio 2013 (en Microsoft Visio 2010 >> botón "Encabezado y pie de página"). Hay algunas opciones para agregar texto como se muestra en la siguiente captura de pantalla. Los usuarios pueden administrar estas propiedades mediante programación usando Aspose.Diagram API de la siguiente manera:

**Administre el texto de los encabezados y pies de página, los márgenes y las propiedades de la fuente.** 

![todo:imagen_alternativa_texto](working-with-headers-and-footers_1.png)

El siguiente fragmento de código ayuda a administrar las propiedades de encabezados y pies de página.
#### **Ejemplos de programación**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
