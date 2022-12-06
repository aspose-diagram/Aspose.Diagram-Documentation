---
title: Aspose.Diagram for .NET 6.3.0 Notas de la versión
type: docs
weight: 90
url: /es/net/aspose-diagram-for-net-6-3-0-release-notes/
---
## **Otras mejoras y cambios**

|**Llave** |**Resumen** |**Categoría** |
|:- |:- |:- |
|DIAGRAMNET-50739 | Agregue soporte para detectar el tipo Visio diagram.| Nueva caracteristica|
|DIAGRAMNET-50746 | Evite la exportación de las páginas ocultas Visio en el PDF.| Nueva caracteristica|
|DIAGRAMNET-50747 | Evite la exportación de las páginas ocultas Visio en el HTML.| Nueva caracteristica|
|DIAGRAMNET-50750 | Evite la exportación de las páginas ocultas Visio en PNG.| Nueva caracteristica|
|DIAGRAMNET-50751 | Evite la exportación de las páginas ocultas Visio en el archivo JPEG.| Nueva caracteristica|
|DIAGRAMNET-50752 | Evite la exportación de las páginas ocultas Visio en el SVG.| Nueva caracteristica|
|DIAGRAMNET-50753 | Evite la exportación de las páginas ocultas Visio en el GIF.| Nueva caracteristica|
|DIAGRAMNET-50754 | Evite la exportación de las páginas ocultas Visio en el XPS.| Nueva caracteristica|
|DIAGRAMNET-50541 | VSDX a la conversión de PDF, los elementos de texto en hebreo se procesan en orden inverso.| Mejora|
|DIAGRAMNET-50542 | VSD a conversión de PDF, la palabra árabe se convierte en letras.| Mejora|
|DIAGRAMNET-50682 | VSD a la exportación de PDF, el texto de la celda de la tabla es parcialmente invisible.| Insecto|
|DIAGRAMNET-50712 | VDX a la exportación de PDF: el texto de varias formas está fuera de lugar.| Insecto|
|DIAGRAMNET-50741 | VSD a la exportación SVG faltan algunas formas Visio.| Insecto|
|DIAGRAMNET-50742 | VSD a la exportación SVG no aplica el color blanco interno de las formas.| Insecto|
|DIAGRAMNET-50744 |La rutina de abrir y guardar de VSDX ha cambiado el texto a caracteres ficticios.| Insecto|
|DIAGRAMNET-50745 | La rutina de abrir y guardar de VSDX ha cambiado el modelador de línea de puntos.| Insecto|
|DIAGRAMNET-50748 | VSD a la exportación de PDF: los elementos de texto están fuera de lugar.| Insecto|
|DIAGRAMNET-50763 | La exportación de VSD a VDX arroja el error del elemento maestro.| Insecto|
### **Public API y cambios incompatibles con versiones anteriores**
Consulte la lista para conocer los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
#### **Agregar clases FileFormatUtil y FileFormatInfo**
Estas clases brindan acceso programático para detectar el tipo de archivo Visio.
#### **Agrega el método DetectFileFormat en la clase FileFormatUtil**
Detecta y devuelve la información sobre el formato de un Visio diagram almacenado en un archivo.
#### **Agrega la propiedad FileFormatType en la clase FileFormatInfo**
Obtiene el formato de archivo detectado.
#### **Agrega la propiedad LoadFormat en FileFormatInfo**
Obtiene el formato de carga detectado.
#### **Agrega la propiedad ExportHiddenPage en las clases SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions y PdfSaveOptions**
Define si es necesario exportar las páginas ocultas Visio o no.
### **Ejemplos de uso**
Consulte la lista de temas de ayuda agregados en los documentos Wiki Aspose.Diagram:

- [Controle la exportación de páginas ocultas Visio al guardar](/diagram/es/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
- [Detectar el formato del archivo Visio](/diagram/es/net/introduction/#detect-the-format-of-visio-file)
