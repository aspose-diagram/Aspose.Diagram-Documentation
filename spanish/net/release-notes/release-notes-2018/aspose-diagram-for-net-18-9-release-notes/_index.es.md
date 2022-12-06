---
title: Aspose.Diagram for .NET 18.9 Notas de la versión
type: docs
weight: 40
url: /es/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51509|VSDX a PNG: pérdida de opacidad de línea en la imagen de salida|Mejora|
|DIAGRAMNET-51510|VSDX a SVG: pérdida de opacidad de línea en la imagen de salida|Mejora|
|DIAGRAMNET-51516|Combinar múltiples archivos VISIO en una sola salida|Mejora|
|DIAGRAMNET-50272|Conversión de VSD a SVG: algunos puntos de conexión tienen una posición y un tamaño incorrectos|Insecto|
|DIAGRAMNET-50273|VSD a SVG: la alineación de los elementos de texto de forma es incorrecta|Insecto|
|DIAGRAMNET-50487|VSD a HTML: el carácter de barra entre el valor está fuera de lugar|Insecto|
|DIAGRAMNET-50975|VSDX a PDF - El color de fondo de la forma es negro|Insecto|
|DIAGRAMNET-50976|VSDX a HTML: el color de fondo de la forma es negro|Insecto|
|DIAGRAMNET-50980|VSDX a PNG: los números dentro de las formas de diamante están fuera de lugar|Insecto|
|DIAGRAMNET-51129|Los elementos de texto no están alineados correctamente al convertir un VSD a PDF|Insecto|
|DIAGRAMNET-51511|Puntas de flecha adicionales en la conversión de PNG|Insecto|
|DIAGRAMNET-51512|Puntas de flecha adicionales que se muestran en la conversión de SVG|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
#### **Se agregó el método Combine en la clase Diagram**
Combina un objeto Diagram con otro objeto Diagram.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
