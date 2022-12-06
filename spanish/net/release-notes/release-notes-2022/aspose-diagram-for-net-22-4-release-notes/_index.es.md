---
title: Aspose.Diagram for .NET 22.4 Notas de la versión
type: docs
weight: 24
url: /es/net/aspose-diagram-for-net-22-4-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 22.4.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-52015|Ticket de continuación de #DIAGRAMNET-51995 - Problemas con los archivos Aspose.Diagram y Skyline Datamine|Mejora|
|DIAGRAMNET-52707|Los cambios en la fórmula o el valor de la hoja de formas no desencadenan cambios en las celdas dependientes|Mejora|
|DIAGRAMNET-50345|VSDX a conversión de PDF, color de fondo incorrecto de las formas|Insecto|
|DIAGRAMNET-50954|Problemas de formato al representar una tabla y un botón de opción al convertir un VSDX a PNG|Insecto|
|DIAGRAMNET-52708|Conversión de posición de texto a svg|Insecto|
|DIAGRAMNET-52739|Formato de puntos sensibles a la cultura|Insecto|
|DIAGRAMNET-52759|El texto presente en la tabla se elimina al convertir el archivo .vsdx a pdf|Insecto|
|DIAGRAMNET-52762|VSDX a PDF - Imagen no convertida|Insecto|
|DIAGRAMNET-52779|Las elipses no se escalan al convertir Visio a SVG|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.
### **Agrega GetPureText en forma**
- Obtener la cadena de texto de una forma.

{{< highlight "java" >}}
String text = shape.GetPureText();
{{< /highlight >}}

