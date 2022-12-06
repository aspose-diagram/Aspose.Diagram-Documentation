---
title: Aspose.Diagram for .NET 21.11 Notas de la versión
type: docs
weight: 2
url: /es/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 21.11.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51111|El relleno degradado de los círculos es incorrecto al convertir un VDX a EMF|Mejora|
|DIAGRAMNET-52377|Agregue soporte para cargar vsd con la versión anterior 3|Mejora|
|DIAGRAMNET-51364|VSDX a PNG: falta el texto del objeto OLE incrustado|Insecto|
|DIAGRAMNET-52329|VSDX a HTML: los emojis no están presentes en la salida|Insecto|
|DIAGRAMNET-52345|El encabezado y el pie de página se pierden después de guardar el archivo Diagram|Insecto|
|DIAGRAMNET-52349|Visio a HTML: se cortan los bordes izquierdo y derecho|Insecto|
|DIAGRAMNET-52374|ArgumentOutOfRangeException al guardar en PDF|Insecto|
|DIAGRAMNET-52386|¿Por qué algunas páginas diagram pueden duplicarse y otras no pueden usar Page.Copy()?|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.


### **Agrega PresetTheme en forma**
- Aplique un tema predeterminado a esta forma.

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **Agrega PresetThemeVariant en Shape**
- Aplicar una variante de tema preestablecido a esta forma

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **Agrega PresetThemeQuickStyle en Shape**
- Aplique un estilo rápido de variante de tema preestablecido a esta forma

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
