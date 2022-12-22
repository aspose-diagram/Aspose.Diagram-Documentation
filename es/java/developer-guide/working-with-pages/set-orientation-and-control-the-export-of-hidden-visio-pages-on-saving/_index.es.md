---
title: Establezca la orientación y controle la exportación de páginas ocultas Visio al guardar
type: docs
weight: 20
url: /es/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Cambiar un diseño de página Visio a vertical u horizontal**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API permite a los desarrolladores establecer la orientación de la página de dibujo Visio mediante programación. Este tema de ayuda explica cómo realizar esta tarea.

 Aspose.Diagram for Java API tiene el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) clase que representa una página de dibujo Visio. La propiedad PageSheet expuesta por la clase Page también expone las propiedades de impresión. El campo PrintPageOrientation de las propiedades de impresión permite rotar la página. Ofrece tres opciones como Retrato, Paisaje y lo mismo que en la impresora. El campo PrintPageOrientation se puede configurar mediante programación usando Aspose.Diagram API.

Este ejemplo funciona de la siguiente manera:

1. Cargue un Visio diagram existente en el objeto de clase Diagram.
1. Extraiga una página Visio
1. Establezca su orientación como Vertical, Horizontal o igual que en la impresora.
1. Aparta el Visio diagram.
### **Muestra de Programación de Orientación de Conjunto**
El siguiente ejemplo de código muestra cómo configurar la orientación de la página Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-SetVisioPageOrientation-SetVisioPageOrientation.java" >}}
## **Controle la exportación de páginas ocultas Visio al guardar**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Oculte una página en Visio Diagram y establezca la opción de exportación**
 Aspose.Diagram for Java API tiene el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) clase que representa una página de dibujo Visio. La propiedad PageSheet expuesta por la clase Page también expone las propiedades de la página. El campo UIVisibility de las propiedades de la página permite ocultar la página. Luego, los desarrolladores pueden usar la propiedad ExportHiddenPage que se agrega en las clases SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions y PdfSaveOptions.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExporToHiddenVisioPagesToPdf-ExporToHiddenVisioPagesToPdf.java" >}}
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToHtml-ExportOfHiddenVisioPagesToHtml.java" >}}
#### **Establecer la opción de exportación para la imagen**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un diagram en formato de imagen.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.java" >}}
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.java" >}}
