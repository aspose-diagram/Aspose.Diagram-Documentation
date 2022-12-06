---
title: Aspose.Diagram for .NET 20.1 Notas de la versión
type: docs
weight: 70
url: /es/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 20.1.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51198|La sombra en el botón de hipervínculo no se representa correctamente al guardar VSDM en SVG|Mejora|
|DIAGRAMNET-51526|VSDX a PDF: relleno degradado para puntas de flecha perdidas en el PDF resultante|Mejora|
|DIAGRAMNET-51539|El degradado en las formas se ha perdido en la salida SVG|Mejora|
|DIAGRAMNET-50705|VSD a exportación SVG: las formas de metatipo se convierten en símbolos desordenados|Insecto|
|DIAGRAMNET-51664|El archivo se corrompe después de eliminar el tema no utilizado|Insecto|
|DIAGRAMNET-51665|Las imágenes se muestran como X después de eliminar los temas no utilizados|Insecto|
|DIAGRAMNET-51684|Al eliminar formas maestras y estilos no utilizados, solo la imagen tiene un problema|Insecto|
|DIAGRAMNET-51726|Falta la imagen de fondo (se agregó PowerPoint en VISIO) al eliminar formas y estilos maestros no utilizados|Insecto|
|DIAGRAMNET-51737|Visio a Html - Problema de tamaño de imagen|Insecto|
|DIAGRAMNET-51743|Eliminación de información privada de Visio: el problema del tamaño del documento Visio|Insecto|
|DIAGRAMNET-51745|Se produce un error extraño en la aplicación WPF al convertir VSD a VSDX|Insecto|

## **Public API y cambios incompatibles con versiones anteriores**
- Páginas agregadas a LoadOptions: especifica el índice de las páginas que se cargarán.



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- Se agregaron SetFontSources en FontConfigs: establece las fuentes de fuentes

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
