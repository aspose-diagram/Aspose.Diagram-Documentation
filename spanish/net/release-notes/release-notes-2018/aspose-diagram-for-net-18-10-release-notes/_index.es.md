---
title: Aspose.Diagram for .NET 18.10 Notas de la versión
type: docs
weight: 30
url: /es/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51527|Las imágenes se pierden después de convertir VSDM a SVG|Mejora|
|DIAGRAMNET-51532|VSD a PDF - La sombra de la imagen no es correcta|Mejora|
|DIAGRAMNET-51536|La sombra de la forma se eliminó después de la conversión VSDX a SVG|Mejora|
|DIAGRAMNET-51544|El subrayado se elimina del texto después de convertir VSDM a SVG|Mejora|
|DIAGRAMNET-51558|Implementar Getter para Shape.ConnectorsType|Mejora|
|DIAGRAMNET-51520|VDX a HTML: aparecen líneas adicionales en la salida|Insecto|
|DIAGRAMNET-51521|La fuente en diagram obtiene cambios después de guardar VSD como VSDX|Insecto|
|DIAGRAMNET-51523|VSDX a SVG - Faltan puntas de flecha|Insecto|
|DIAGRAMNET-51524|VSDM a SVG - Aparecieron cruces azules en el archivo de salida|Insecto|
|DIAGRAMNET-51525|La forma de decisión cambia de diamante a cuadrado mientras que VSDM a conversión SVG|Insecto|
|DIAGRAMNET-51528|La forma de decisión cambia de diamante a cuadrado mientras que VSDM a conversión SVG|Insecto|
|DIAGRAMNET-51529|VSDM a SVG - Líneas punteadas convertidas en líneas rellenas|Insecto|
|DIAGRAMNET-51531|Las formas se desplazan hacia el lado derecho después de convertir VSDX a SVG|Insecto|
|DIAGRAMNET-51533|Aparecieron cruces rojas después de la conversión de VISIO a SVG|Insecto|
|DIAGRAMNET-51534|Apareció un punto rojo en la esquina inferior izquierda de la forma|Insecto|
|DIAGRAMNET-51538|Las imágenes se pierden después de convertir VSDX a PDF|Insecto|
|DIAGRAMNET-51541|El texto se vuelve invisible después de convertir VSDX a SVG|Insecto|
|DIAGRAMNET-51542|El texto se eliminó después de la conversión VSDX a SVG|Insecto|
|DIAGRAMNET-51543|El formato de hora y fecha se cambia después de VSDM A SVG|Insecto|
|DIAGRAMNET-51545|VSDX a SVG: el texto está envuelto en la salida|Insecto|
|DIAGRAMNET-51546|VSDX a SVG: el texto está envuelto en la salida|Insecto|
|DIAGRAMNET-51547|VSDX a SVG: el texto está envuelto en la salida|Insecto|
|DIAGRAMNET-51548|VSDX a SVG: el texto está envuelto en la salida|Insecto|
|DIAGRAMNET-51551|No se puede obtener el color de tema correcto de las formas|Insecto|
|DIAGRAMNET-51552|Puntas de flecha invertidas que se muestran en la conversión de SVG|Insecto|
|DIAGRAMNET-51559|Problema de cambio de tamaño de texto al convertir VSDM a SVG|Insecto|
|DIAGRAMNET-51560|Las líneas de conexión se vuelven delgadas después de convertir a SVG|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
#### **Se agregó InheritLine en Shape**
Contiene los valores de formato de línea para la forma heredada por el estilo principal y la forma maestra.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **Se agregó GetConnectorsType en Shape**
Obtener tipo de conectores

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

