---
title: Aspose.Diagram for .NET 17.8 Notas de la versión
type: docs
weight: 50
url: /es/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX a SVG - la baja calidad de la salida SVG.|Mejora|
|DIAGRAMNET-51298|SVGSaveOptions: agregue soporte para controlar el nivel de compresión de mapa de bits.|Mejora|
|DIAGRAMNET-51300|Agregue soporte para conectar formas con índice de conexión.|Mejora|
|DIAGRAMNET-50577|VSDX a conversión de PDF, el texto de la forma circular está fuera de lugar - I.|Insecto|
|DIAGRAMNET-50582|VSDX a la conversión de HTML, el texto de la forma circular está fuera de lugar - I.|Insecto|
|DIAGRAMNET-50601|VSDX a conversión de PDF, el texto de la forma circular está fuera de lugar - II.|Insecto|
|DIAGRAMNET-50606|VSDX a la conversión de HTML, el texto de la forma circular está fuera de lugar - II.|Insecto|
|DIAGRAMNET-51197|Las formas de los triángulos de advertencia no se representan correctamente al guardar VSDM en SVG.|Insecto|
|DIAGRAMNET-51245|Elementos de texto desplazados al convertir un VSD a PDF.|Insecto|
|DIAGRAMNET-51246|Se aplicaron fuentes incorrectas al texto al convertir un VSD a PDF.|Insecto|
|DIAGRAMNET-51296|VSDM a SVG: la imagen está truncada.|Insecto|
|DIAGRAMNET-51301|VSDX a PDF: se cambia el color del texto en las líneas de conexión.|Insecto|
|DIAGRAMNET-51302|VSDX a PDF - faltan elementos gráficos.|Insecto|
|DIAGRAMNET-51304|VSDX a PDF - representación incompleta del diagrama de flujo.|Insecto|
|DIAGRAMNET-51305|VSDX a PDF - faltan elementos gráficos.|Insecto|
|DIAGRAMNET-51306|VSDX a PDF: se cambia el color del texto en las líneas de conexión.|Insecto|
|DIAGRAMNET-51307|VSDX a PDF - faltan elementos gráficos.|Insecto|
|DIAGRAMNET-51313|La rutina de abrir y guardar de un dibujo VSDX genera un archivo de salida corrupto.|Insecto|
|DIAGRAMNET-51314|VSDX a SVG - posicionamiento incorrecto del texto.|Insecto|
|DIAGRAMNET-51317|VSDX a PDF: falta el texto de las líneas de conexión.|Insecto|
|DIAGRAMNET-51318|VSDX a PDF: falta el texto en negrita de las formas rectangulares.|Insecto|
|DIAGRAMNET-51319|VSDM a SVG: la operación aritmética resultó en un error de desbordamiento.|Insecto|
|DIAGRAMNET-51320|Error en el elemento de forma al cargar un VSDM.|Insecto|
|DIAGRAMNET-51323|VSDM a SVG: faltan todas las líneas de conexión.|Insecto|
|DIAGRAMNET-51324|VSDM a SVG: estilo de borde incorrecto y color de borde de varias formas.|Insecto|
|DIAGRAMNET-51326|Problema después de agregar dos comentarios a la forma.|Insecto|
|DIAGRAMNET-51327|Problema después de usar el método "AddComment" al agregar comentarios a varias formas.|Insecto|
|DIAGRAMNET-51328|Aspose Diagram importa incorrectamente la forma al documento.|Insecto|
|DIAGRAMNET-51330|VSDM a SVG: se agrega un texto de marca de agua adicional.|Insecto|
|DIAGRAMNET-51332|VSDM a SVG: representación incorrecta de un icono.|Insecto|
|DIAGRAMNET-51334|VSDM a SVG: texto desplazado en la esquina superior derecha.|Insecto|
|DIAGRAMNET-51335|VSDM a SVG: representación incorrecta de la imagen de fondo.|Insecto|
|DIAGRAMNET-51337|VSD a HTML: formato no válido del error de cadena de entrada.|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **Agrega miembro de calidad en la clase SVGSaveOptions**
Obtiene o establece un valor que determina la calidad de las imágenes generadas.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Agrega el método ConnectShapesViaConnectorIndex en la clase Page**
Permite conectar formas utilizando índices de conexión.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Ejemplos de uso**
Consulte la lista de temas de ayuda agregados en los documentos Wiki Aspose.Diagram:

1. [Usar índices de conexión para conectar formas](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [Uso de las opciones de guardado de SVG](https://docs.aspose.com/diagram/net/save-visio-document/)
