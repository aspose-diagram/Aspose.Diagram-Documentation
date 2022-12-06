---
title: Establezca la orientación y controle la exportación de páginas ocultas Visio al guardar
type: docs
weight: 20
url: /es/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: Esta sección explica cómo configurar el diseño de la página con Aspose.Diagram.
---
## **Cambiar un diseño de página Visio a vertical u horizontal**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API permite a los desarrolladores establecer la orientación de la página de dibujo Visio mediante programación. Este tema de ayuda explica cómo realizar esta tarea.

 Aspose.Diagram for .NET API tiene el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) clase que representa una página de dibujo Visio. La propiedad PageSheet expuesta por la clase Page también expone las propiedades de impresión. El campo PrintPageOrientation de las propiedades de impresión permite rotar la página. Ofrece tres opciones como Retrato, Paisaje y lo mismo que en la impresora. El campo PrintPageOrientation se puede configurar mediante programación usando Aspose.Diagram API.

Este ejemplo funciona de la siguiente manera:

1. Cargue un Visio diagram existente en el objeto de clase Diagram.
1. Extraiga una página Visio
1. Establezca su orientación como Vertical, Horizontal o igual que en la impresora.
1. Aparta el Visio diagram.
### **Muestra de Programación de Orientación de Conjunto**
El siguiente ejemplo de código muestra cómo configurar la orientación de la página Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Controle la exportación de páginas ocultas Visio al guardar**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API permite a los desarrolladores incluir o excluir Visio páginas ocultas al guardar diagram en archivos PDF, HTML, de imagen (PNG, JPEG, GIF), SVG y XPS. Incluso pueden ocultar Visio páginas usando Aspose.Diagram API porque su opción ya está disponible a través de la celda UIVisibility en la página ShapeSheet.
### **Oculte una página en Visio Diagram y establezca la opción de exportación**
 Aspose.Diagram for .NET API tiene el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) clase que representa una página de dibujo Visio. La propiedad PageSheet expuesta por la clase Page también expone las propiedades de la página. El campo UIVisibility de las propiedades de la página permite ocultar la página. Luego, los desarrolladores pueden usar la propiedad ExportHiddenPage que se agrega en las clases SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions y PdfSaveOptions.
#### **Establecer la opción de exportación para PDF**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un diagram en formato PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **Establecer la opción de exportación para HTML**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un diagram en formato HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Establecer la opción de exportación para la imagen**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un diagram en formato de imagen.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **Establecer la opción de exportación para SVG**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un diagram en formato SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **Establecer la opción de exportación para XPS**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un diagram en formato XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
