---
title: Aspose.Diagram for .NET 17.7 Notas de la versión
type: docs
weight: 60
url: /es/net/aspose-diagram-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for .NET 17.7](https://www.nuget.org/packages/Aspose.Diagram/17.7.0).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51204|El tamaño del papel de la impresora se cambia después de guardar diagram.|Mejora|
|DIAGRAMNET-51230|Valores incorrectos de los márgenes de página.|Mejora|
|DIAGRAMNET-51274|Agregue soporte para insertar comentarios en el nivel de forma.|Mejora|
|DIAGRAMNET-51297|Entrada VDX: lectura incorrecta de SolutionXML.|Mejora|
|DIAGRAMNET-51061|Faltan formas al convertir un VST a PNG.|Insecto|
|DIAGRAMNET-51262|Elementos de texto desplazados al convertir un VSDM a SVG.|Insecto|
|DIAGRAMNET-51276|VSD a SVG: todos los íconos no se ven correctamente.|Insecto|
|DIAGRAMNET-51277|VSDM a SVG: falta la sombra de las formas.|Insecto|
|DIAGRAMNET-51279|Falta un carácter al convertir un VSD a PDF.|Insecto|
|DIAGRAMNET-51282|Algunos archivos vdx están dañados después de guardar.|Insecto|
|DIAGRAMANET-51284-|DiagramException ocurre en la carga del archivo vsdx.|Insecto|
|DIAGRAMNET-51285|VSD a PNG: faltan todos los elementos de texto.|Insecto|
|DIAGRAMNET-51286|VSD a PNG: la representación parcial de una forma.|Insecto|
|DIAGRAMNET-51288|Error de valor de color no válido al convertir un VSDX a PNG.|Insecto|
|DIAGRAMNET-51289|El icono de comentarios a nivel de página no muestra texto.|Insecto|
|DIAGRAMNET-51290|Aspose.Diagram error en el método SetWidth.|Insecto|
|DIAGRAMNET-51291|Salida VSDX: diseño incorrecto al establecer las líneas de conexión rectas.|Insecto|
|DIAGRAMNET-51292|Salida VSDX: el elemento de texto de las líneas de conexión está fuera de lugar.|Insecto|
|DIAGRAMNET-51293|VSDX a SVG: aparece una marca adicional junto con las formas.|Insecto|
|DIAGRAMNET-51294|VSDM a SVG: aparece una marca adicional junto con las formas.|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **El método AddComment se agrega en la clase de página**
Un método AddComment sobrecargado, expuesto por la clase Page, toma una instancia de la clase Shape y una cadena de texto del comentario.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Ejemplos de uso**
Consulte la lista de temas de ayuda agregados en los documentos Wiki Aspose.Diagram:

1. [Agregue un comentario de nivel de forma en el dibujo Visio](/diagram/es/net/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
