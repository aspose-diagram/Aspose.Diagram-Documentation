---
title: Aspose.Diagram for .NET 20.10 Notas de la versión
type: docs
weight: 10
url: /es/net/aspose-diagram-for-net-20-10-release-notes/
---
{{% alert color="primary" %}}

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 20.10.

{{% /alert %}}
## **Mejoras y Cambios**  ##

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51891|Visio a JPG - API está tardando mucho en convertirse|Mejora|
|DIAGRAMNET-51902|Los archivos Visio con versiones inferiores a 11 no son compatibles, excepto al abrir VSS|Mejora|
|DIAGRAMNET-51906|Exportar VSDX a PDF: problemas con el ancho de línea, la imagen y el dimensionamiento|Mejora|
|DIAGRAMNET-51929|Conversión de VSD a SVG: Transformaciones de matriz en el archivo SVG de salida|Mejora|
|DIAGRAMNET-51931|Visio a PDF - API consume una gran cantidad de memoria y lleva mucho tiempo|Mejora|
|DIAGRAMNET-51936|[Cont.]Visio a PDF - API consume una gran cantidad de memoria y tarda mucho tiempo|Mejora|
|DIAGRAMNET-51881|La posición de 2 etiquetas no es correcta|Insecto|
|DIAGRAMNET-51907|Ocurrió un error genérico en la excepción GDI+ al procesar el archivo VSDX|Insecto|
|DIAGRAMANET-51926-|Aspose.Diagram 20.9: NullReferenceException al convertir VDX a PNG|Insecto|
|DIAGRAMNET-51928|Conversión de VSD a SVG: faltan algunas flechas y texto al final de las líneas|Insecto|
|DIAGRAMNET-51932|Estilos de forma perdidos después de la conversión vsd -> vsdx|Insecto|
|DIAGRAMNET-51933|El gradiente detiene el formato que no cumple con el estándar svg|Insecto|
|DIAGRAMNET-51934|Object reference not set to an instance of an object.' when saving VSS shapes for specific file|Insecto|
|DIAGRAMNET-51940|La posición de 2 etiquetas no es correcta|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**  ##
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.

 * Se agregó IsExportScaleInMatrix en SVGSaveOptions: define si es necesario exportar la escala en la matriz o no.
```
Aspose.Diagram.Saving.SVGSaveOptions o = new Aspose.Diagram.Saving.SVGSaveOptions();
o.IsExportScaleInMatrix = false;
```
