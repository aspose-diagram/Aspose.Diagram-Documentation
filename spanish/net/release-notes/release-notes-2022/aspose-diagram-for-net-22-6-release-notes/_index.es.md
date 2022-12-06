---
title: Aspose.Diagram for .NET 22.6 Notas de la versión
type: docs
weight: 22
url: /es/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 22.6.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-52826|Enlace roto al guardar VSDM en PDF|Mejora|
|DIAGRAMNET-52851|Algunas formas pierden su curva después de la conversión a svg|Mejora|
|DIAGRAMNET-52858|Calidad de imagen en HTML|Mejora|
|DIAGRAMNET-52825|Exportar a HTML problema|Insecto|
|DIAGRAMNET-52832|Visio a PDF/SVG - Se cambió la posición del texto rotado|Insecto|
|DIAGRAMNET-52840|Elementos en la vista previa de HTML borrosos|Insecto|
|DIAGRAMNET-52842|La página de ajuste automático no se ajusta automáticamente|Insecto|
|DIAGRAMNET-52849|Las imágenes ráster no se reducen después de la conversión|Insecto|
|DIAGRAMNET-52852|VSD Error de apertura - Aspose.Diagram.DiagramException|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.
### **Agrega resolución en HTMLSaveOptions**
- Obtiene o establece la resolución del html generado, en puntos por pulgada.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
