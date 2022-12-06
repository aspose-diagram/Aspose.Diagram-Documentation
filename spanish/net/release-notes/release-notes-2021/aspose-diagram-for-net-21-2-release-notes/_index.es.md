---
title: Aspose.Diagram for .NET 21.2 Notas de la versión
type: docs
weight: 11
url: /es/net/aspose-diagram-for-net-21-2-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 21.2.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51986|Agregue el método centerDrawing presente en la página de interoperabilidad visio|Mejora|
|DIAGRAMNET-51987|Implementar un método para obtener ActivePage|Mejora|
|DIAGRAMNET-51978|Convierta VSD a VSDX: no se puede abrir la salida en MS Visio|Insecto|
|DIAGRAMNET-51980|"Se produjo un error genérico en GDI+". excepción al renderizar al archivo HTML VSDX|Insecto|
|DIAGRAMNET-51981|Convierta VSDX a PDF: las formas son negras en el pdf de salida|Insecto|
|DIAGRAMNET-51985|Conversión de VSDX a VSDX/VDX: los colores de forma cambian a degradado después de guardar|Insecto|
|DIAGRAMNET-51989|Visio a HTML - Borde extraño en la salida|Insecto|

## ` `**Public API y cambios incompatibles con versiones anteriores**
` ` La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.
### **Se agregó ActivePage en Diagram**
- Especifica la página activa

{{< highlight "java" >}}

Page page = diagram.ActivePage;

{{< /highlight >}}
### **Agrega dibujo central en forma**
- Centrar la forma con respecto a la extensión de la página



{{< highlight "java" >}}

shape.CenterDrawing()

{{< /highlight >}}
### **Agrega DrawLine en la página**
- El proceso de dibujar una sola línea.



{{< highlight "java" >}}

 diagram.Pages[0].DrawLine(0,0,1,1);

{{< /highlight >}}



