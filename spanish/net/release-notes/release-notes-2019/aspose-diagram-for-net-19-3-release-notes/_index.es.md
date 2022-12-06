---
title: Aspose.Diagram for .NET 19.3 Notas de la versión
type: docs
weight: 100
url: /es/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene notas de la versión para[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-50930|Agregue soporte para recuperar directorios de fuentes comunes en sistemas operativos|Mejora|
|DIAGRAMNET-51614|Obtenga todos los valores de accesorios para una forma|Mejora|
|DIAGRAMNET-50214|VSD a conversión de PDF - Las líneas curvas se convierten en una línea recta|Insecto|
|DIAGRAMNET-50240|Conversión de VSD a PDF: disposición incorrecta de los conectores dinámicos|Insecto|
|DIAGRAMNET-50703|VSDX a la exportación de PDF: falta un conector dinámico|Insecto|
|DIAGRAMNET-50704|VSD a exportación de PDF: las formas de metatipo se convierten en símbolos desordenados|Insecto|
|DIAGRAMNET-51535|VSDM a SVG - Cambios de fuente de Sans a Serif en SVG|Insecto|
|DIAGRAMNET-51574|VSDX a PNG: algunas formas se representan incorrectamente en la salida PNG|Insecto|
|DIAGRAMNET-51608|Ajuste de texto no funciona como se esperaba|Insecto|
|DIAGRAMNET-51609|Las formas se desplazan hacia el lado izquierdo cuando se copia Diagram en PowerPoint Diapositiva|Insecto|
|DIAGRAMNET-51617|Visio a PDF: los valores controlados por datos externos no se muestran correctamente|Insecto|
|DIAGRAMNET-51619|Visio a PDF - Fecha/Hora/Distancia incorrecta en PDF|Insecto|
|DIAGRAMNET-51621|Visio a PDF: la imagen de fondo está distorsionada y la página adicional está presente en PDF|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **Agrega GetDefaultFontDir en Diagram**
Obtener la ruta de la carpeta Fuentes predeterminadas

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
