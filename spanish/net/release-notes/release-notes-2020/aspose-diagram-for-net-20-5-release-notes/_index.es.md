---
title: Aspose.Diagram for .NET 20.5 Notas de la versión
type: docs
weight: 30
url: /es/net/aspose-diagram-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 20.5.

{{% /alert %}} 
## **Mejoras y Cambios**
VSD a conversión de PDF, no se conserva la alineación correcta del texto de las formas

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51088|Recupera el recuento de páginas incorrecto de un VSD|Mejora|
|DIAGRAMNET-51731|Determine si una forma se cruza con otra forma en el diagram|Mejora|
|DIAGRAMNET-51833|Aspose.Diagram 20.4: Visio La versión del documento no es compatible|Mejora|
|DIAGRAMNET-50361|VSD a conversión de PDF, no se conserva la alineación correcta del texto de las formas|Insecto|
|DIAGRAMNET-50955|Los elementos de texto de las formas de diamante se desplazan al convertir un VSDX a PNG|Insecto|
|DIAGRAMNET-50990|Además, los signos negativos y de dólar no están correctamente alineados al convertir un VSDX a PNG.|Insecto|
|DIAGRAMNET-51815|Una gran cantidad de líneas de texto en forma podría crear obviamente un desplazamiento en la parte inferior|Insecto|
|DIAGRAMNET-51820|La marca de agua de evaluación no cabe en una página|Insecto|
|DIAGRAMNET-51821|Visio a Html: problemas de imagen y enlaces en la salida|Insecto|
|DIAGRAMNET-51823|Mientras convierte Visio a SVG. Algunas imágenes tienen problemas. Falta el icono.|Insecto|
|DIAGRAMNET-51824|Mientras convierte Visio a SVG. Alineación de contenido incorrecta|Insecto|
|DIAGRAMNET-51826|Mientras convierte Visio a SVG. Falta el icono|Insecto|
|DIAGRAMNET-51827|Al convertir Visio a SVG - Falta el código QR|Insecto|
|DIAGRAMNET-51828|Al convertir Visio a SVG - Falta el ícono de PDF|Insecto|
|DIAGRAMNET-51829|Al convertir Visio a SVG - Icono perdido (Falta)|Insecto|
|DIAGRAMNET-51830|Al convertir Visio a SVG - Imagen perdida (Falta)|Insecto|
|DIAGRAMNET-51831|Visio a HTML: problemas de imagen y enlaces en la salida|Insecto|
|DIAGRAMNET-51834|Visio guardar HTML - conectores incorrectos|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.
### **Agrega IsIntersect en Shape**
- Indica si esta forma se cruza con otra forma.

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



