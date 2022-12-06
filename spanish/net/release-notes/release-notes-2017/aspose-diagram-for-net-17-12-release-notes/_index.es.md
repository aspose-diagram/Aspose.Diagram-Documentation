---
title: Aspose.Diagram for .NET 17.12 Notas de la versión
type: docs
weight: 10
url: /es/net/aspose-diagram-for-net-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for .NET 17.12](https://www.nuget.org/packages/Aspose.Diagram/17.12.0).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-50016|Agregue soporte para duplicar / clonar una forma|Mejora|
|DIAGRAMNET-50677|Proporcione el único API para convertir una forma Visio a PDF|Mejora|
|DIAGRAMNET-50678|Proporcione el único API para convertir una forma Visio a HTML|Mejora|
|DIAGRAMNET-50762|Se produjo el error de análisis del valor de los atributos largos al generar un VDX diagram|Insecto|
|DIAGRAMNET-51401|Salida VSDX: los controles en Formas no funcionan|Insecto|
|DIAGRAMNET-51402|VSDX a la imagen: no se conserva un objeto OLE|Insecto|
|DIAGRAMNET-51406|VSD a la imagen - aparecen los caracteres adicionales|Insecto|
|DIAGRAMNET-51410|VSD a PDF - el número de página sigue siendo 4 en todas las páginas|Insecto|
|DIAGRAMNET-51411|VSD a la imagen - el número de página sigue siendo 4 en todas las páginas|Insecto|
|DIAGRAMNET-51414|VSDX a PDF: falta el contenido de las formas|Insecto|
|DIAGRAMNET-51415|VSDX a PDF - color de fondo incorrecto de las formas|Insecto|
|DIAGRAMNET-51416|VSDX a HTML: color de fondo incorrecto de las formas|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **Agrega miembro de copia en la clase de forma**
El miembro de copia toma una instancia de forma de destino como parámetro para clonar esta forma.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
### **Agrega miembro ToPdf en la clase Shape**
El miembro ToPdf convierte una forma al formato PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf("e:\\out.pdf");

{{< /highlight >}}
### **Agrega miembro ToHTML en la clase Shape**
El miembro ToHTML convierte una forma al formato PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML("e:\\out.pdf", hs);

{{< /highlight >}}
### **Ejemplos de uso**
Consulte la lista de temas de ayuda agregados en los documentos Wiki Aspose.Diagram:

1. [Copie una forma Visio en otra instancia de forma](/diagram/es/net/add-2c-retrieve-2c-copy-and-read-visio-shape-data-html/#add-retrieve-copyandreadvisioshapedata-copyavisioshapetoanothershapeinstance)
1. [Convertir Visio Forma a PDF](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-pdf/)
1. [Convertir Visio Forma a HTML](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-html/)
