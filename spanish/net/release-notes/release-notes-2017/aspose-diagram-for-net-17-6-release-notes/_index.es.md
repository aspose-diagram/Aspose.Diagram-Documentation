---
title: Aspose.Diagram for .NET 17.6 Notas de la versión
type: docs
weight: 70
url: /es/net/aspose-diagram-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for .NET 17.6](https://www.nuget.org/packages/Aspose.Diagram/17.6.0).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51264|La sombra de las formas es negra al convertir un VSDM a SVG|Mejora|
|DIAGRAMNET-51270|No se puede ver una forma de VSDX en Visio Viewer|Mejora|
|DIAGRAMNET-51273|Visualización incorrecta de la forma en el Visio Viewer 2013|Mejora|
|DIAGRAMNET-51249|La apariencia incorrecta de la línea curva que conecta en VSDM|Insecto|
|DIAGRAMNET-51250|Se agrega un paréntesis izquierdo adicional en el texto al convertir un VSD a PDF|Insecto|
|DIAGRAMNET-51251|El tamaño del ícono se reduce al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51253|Color incorrecto del texto y los bordes en las formas al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51255|Se ha aplastado una imagen en la parte inferior al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51258|Abra y guarde la rutina de VSDM: se cambia la longitud de las paredes|Insecto|
|DIAGRAMNET-51259|Abra y guarde la rutina de VSDM: se cambia la longitud de las paredes|Insecto|
|DIAGRAMNET-51260|Se produjo un error de índice fuera de rango al llamar al método de diseño de la clase Diagram|Insecto|
|DIAGRAMNET-51263|Aparece una etiqueta de color rojo adicional al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51265|La fuente del texto del título se cambia al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51266|El tamaño de la imagen de fondo se reduce a convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51267|El tamaño de un ícono se reduce al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51268|Recupera el valor de transparencia incorrecto de una imagen del dibujo VSDM|Insecto|
|DIAGRAMNET-51269|Agregar protección de virtualización|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **Agrega miembro RefreshData en la clase de forma**
El método RefreshData de la instancia de la clase Shape actualiza los datos de la forma, incluidos XForm, TextXForm, Connection y Geom, después de cambiar el texto de la forma u otros.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set PinX and PinY values

shape.XForm.PinX.Value = 5;

shape.XForm.PinY.Value = 5;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
