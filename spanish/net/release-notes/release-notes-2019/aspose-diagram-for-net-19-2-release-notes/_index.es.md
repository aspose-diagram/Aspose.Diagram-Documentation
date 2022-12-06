---
title: Aspose.Diagram for .NET 19.2 Notas de la versión
type: docs
weight: 110
url: /es/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene notas de la versión para[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-50009|La forma del corazón se confunde al exportar el dibujo VSD en formato de archivo PDF|Mejora|
|DIAGRAMNET-50010|VSD a PDF exporta múltiples líneas en zigzag con un punto concurrente en lugar de una sola línea curva|Mejora|
|DIAGRAMNET-51257|Agregue soporte de línea NUBRS al exportar un dibujo|Mejora|
|DIAGRAMNET-51611|No se puede obtener Prop.Prompt.Value correctamente|Mejora|
|DIAGRAMNET-50355|Las líneas curvas se exportan como líneas rectas|Insecto|
|DIAGRAMNET-50702|VSDX a exportación PDF - los conectores curvos se vuelven rectos|Insecto|
|DIAGRAMNET-51348|VSDX a PDF - Representación incorrecta de letras|Insecto|
|DIAGRAMNET-51399|VSD a PNG: la línea curva se convierte en línea recta|Insecto|
|DIAGRAMNET-51448|VSD a PNG: falta la elipse alrededor de la palabra red|Insecto|
|DIAGRAMNET-51472|VSD a PDF: las líneas curvas se exportan como líneas rectas|Insecto|
|DIAGRAMNET-51507|VSDX a PNG: faltan formas ovaladas rellenas en la salida|Insecto|
|DIAGRAMNET-51508|VSDX a SVG: faltan formas ovaladas rellenas en la salida|Insecto|
|DIAGRAMNET-51537|VSDX a SVG: los conectores curvos se convierten en conectores rectos cuando VSDX se representa en PDF|Insecto|
|DIAGRAMNET-51540|Los bordes de la forma se cambiaron a cuadrados después de la conversión|Insecto|
|DIAGRAMNET-51577|VISIO a SVG: la salida no es correcta|Insecto|
|DIAGRAMNET-51592|Las líneas curvas se están convirtiendo en líneas rectas durante la conversión|Insecto|
|DIAGRAMNET-51600|Las líneas rectas se convierten en picos al guardar un diagram como otro formato|Insecto|
|DIAGRAMNET-51604|VSDX a error de conversión de PDF - puntos suspensivos negros|Insecto|
|DIAGRAMNET-51605|Actualice las referencias API y agregue detalles sobre el método Shape.SetAngle()|Insecto|
|DIAGRAMNET-51610|VSDX a SVG: el texto no se muestra en la fuente correcta|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **Añadir InheritProps en forma**
Contiene los accesorios para la forma heredada por la forma maestra.

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
