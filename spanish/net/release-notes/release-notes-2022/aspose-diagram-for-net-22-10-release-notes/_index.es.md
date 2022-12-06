---
title: Aspose.Diagram for .NET 22.10 Notas de la versión
type: docs
weight: 18
url: /es/net/aspose-diagram-for-net-22-10-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 22.10.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-52988|Un gráfico se muestra en mala calidad cuando se exporta a formato SVG|Mejora|
|DIAGRAMNET-53002|Pérdida de enlace al exportar a html con Aspose.Diagram|Mejora|
|DIAGRAMNET-52983|Error en Diagram.Guardar|Insecto|
|DIAGRAMNET-52984|Cambiar valores en la clase VentureLicenser|Insecto|
|DIAGRAMNET-52993|La conversación de vsdx a svg falla|Insecto|
|DIAGRAMNET-52995|Aplicación: la carga vsd arroja una excepción|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.

### **Agrega GetDisplayText en forma**
- Obtener el texto que se muestra en la interfaz

{{< highlight "java" >}}
String text = shape.GetDisplayText();
{{< /highlight >}}

### **Agrega InheritGeoms en Shape**
- Contiene los valores de Geoms para la forma heredada por la forma maestra.

{{< highlight "java" >}}
int count = shape.InheritGeoms.Count;
{{< /highlight >}}