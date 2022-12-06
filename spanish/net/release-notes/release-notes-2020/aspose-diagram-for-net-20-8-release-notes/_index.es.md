---
title: Aspose.Diagram for .NET 20.8 Notas de la versión
type: docs
weight: 14
url: /es/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 20.8.

{{% /alert %}}
## **Mejoras y Cambios**  ##

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51886|Cree la capacidad de insertar objetos Ole como palabras, celdas, diapositivas, etc. en el Diagram en la forma única con los datos del objeto y la imagen de vista previa en su interior.|Mejora|
|DIAGRAMNET-51888|Visio a PDF - API está tardando mucho en convertirse|Mejora|
|DIAGRAMNET-51889|Guardar en pdf en bucle más de 20 minutos|Mejora|
|DIAGRAMNET-51893|Falta el atributo viewBox después de la conversión VSDX a SVG|Mejora|
|DIAGRAMNET-51851|VSDX a PDF: faltan algunos íconos y otros no se representan correctamente|Insecto|
|DIAGRAMNET-51873|VSDX a PDF: el contenido está a la izquierda en el PDF de salida|Insecto|
|DIAGRAMNET-51874|VSDX a PDF: falta contenido y líneas en la salida|Insecto|
|DIAGRAMNET-51876|VSDX a PNG: algunas formas son incorrectas en la salida|Insecto|
|DIAGRAMNET-51879|Visio a PDF - la salida no es correcta|Insecto|
|DIAGRAMNET-51894|System.NullReferenceException al cargar el diagram|Insecto|
|DIAGRAMNET-51895|No se pueden recuperar datos de propiedad de grupo como SelectionModel, DisplayMode|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**  ##
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.

####  Método agregado AddShape en la página ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
