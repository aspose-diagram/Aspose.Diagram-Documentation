---
title: Público API Cambios en Aspose.Diagram 6.3.0
type: docs
weight: 30
url: /es/net/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 6.0.0 a la 6.3.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
## **Detectar el formato de un archivo Visio**
**Se agregan varias clases, métodos y propiedades para detectar el formato.**
- **Agregar clases FileFormatUtil y FileFormatInfo** 
 - Estas clases otorgan acceso programático para detectar el tipo de archivo Visio.
- **Agrega el método DetectFileFormat en la clase FileFormatUtil** 
 - Detecta y devuelve la información sobre el formato de un Visio diagram almacenado en un archivo.
- **Agrega la propiedad FileFormatType en la clase FileFormatInfo** 
 - Obtiene el formato de archivo detectado.
- **Agrega la propiedad LoadFormat en FileFormatInfo** 
 - Obtiene el formato de carga detectado.

 Los desarrolladores pueden detectar fácilmente el formato de cualquier archivo Visio. Este tema de ayuda ilustra cómo detectar el formato de archivo Visio (usando una ruta de archivo o secuencia) y verificar su extensión:[Detectar el formato del archivo Visio](/diagram/es/net/introduction/#detect-the-format-of-visio-file)
## **Controle la exportación de páginas ocultas Visio al guardar**
**Agrega la propiedad ExportHiddenPage en las clases SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions y PdfSaveOptions**
- Define si es necesario exportar las páginas ocultas Visio o no.

 Los desarrolladores pueden incluir o excluir Visio páginas ocultas al guardar un Visio diagram en archivos PDF, HTML, de imagen (PNG, JPEG, GIF), SVG y XPS. Este tema de ayuda ilustra cómo hacerlo:[Controle la exportación de páginas ocultas Visio al guardar](/diagram/es/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
