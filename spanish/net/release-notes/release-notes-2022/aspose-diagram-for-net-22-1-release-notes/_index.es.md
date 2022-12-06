---
title: Aspose.Diagram for .NET 22.1 Notas de la versión
type: docs
weight: 27
url: /es/net/aspose-diagram-for-net-22-1-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 22.1.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-50560|Admite guardar diagramas en HTML con o sin recursos integrados|Mejora|
|DIAGRAMNET-52499|Agregue soporte para guardar html en una transmisión única|Mejora|
|DIAGRAMNET-50562|VSDX a PDF: faltan formas en la salida|Insecto|
|DIAGRAMNET-50780|Las líneas de borde de las tablas no son visibles al guardar un VSDX en PDF|Insecto|
|DIAGRAMNET-50962|Faltan las líneas de borde de las tablas al convertir un VSDX a PNG|Insecto|
|DIAGRAMNET-50992|La línea del borde izquierdo de la tabla no es visible al convertir un VSDX a PDF|Insecto|
|DIAGRAMNET-51034|Falta el sombreado de las formas al convertir un VSDX a PDF|Insecto|
|DIAGRAMNET-51186|Diseño incorrecto de formas de tipo meta al convertir un VSD a PDF|Insecto|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0: Guardar en flujo HTML no incrustar recursos externos|Insecto|
|DIAGRAMNET-52506|Page.Copy() no copia los cambios del desarrollador|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.


### **Agrega SaveAsSingleFile en HTMLSaveOptions**
- Indica si guardar el html como archivo único.

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}