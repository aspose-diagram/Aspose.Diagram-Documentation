---
title: Trabajar con imágenes
type: docs
weight: 60
url: /es/net/working-with-images/
description: Esta sección explica cómo insertar u obtener una imagen de una página visio con Aspose.Diagram.
---
## **Extraiga todas las imágenes de una página Visio**
En Microsoft Visio, las páginas son páginas de primer plano o de fondo. Puede extraer imágenes de una página particular de un archivo Visio.
### **Extraer imágenes**
El objeto Clase de página representa el área de dibujo de una página de primer plano o una página de fondo. La propiedad Shapes expuesta por la clase Diagram admite una colección de objetos Aspose.Diagram.Shape. Esta propiedad se puede utilizar para extraer todas las imágenes de una página en particular.
#### **Muestra de programación de extracción de imágenes**
El siguiente fragmento de código extrae todas las imágenes de una página Visio en particular.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **Obtener íconos de varias formas Visio**
Aspose.Diagram for .NET API ahora permite a los desarrolladores obtener íconos de varias Visio formas.
### **Obtener el icono de forma**
El código de los ejemplos siguientes muestra cómo:

1. Cargue un diagram o plantilla existente.
1. Obtener maestro por su índice
1. Obtener icono maestro.
1. Guardar icono en el espacio local.
#### **Muestra de Programación de Obtener Iconos**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **Reemplace una forma de imagen del Visio Diagram**
Aspose.Diagram for .NET API permite a los desarrolladores acceder y reemplazar formas de imagen disponibles en Visio diagram.
### **Sustitución de una forma de imagen**
El código de los ejemplos siguientes muestra cómo:

1. Cargue un diagram existente.
1. Iterar a través de las formas de página selectivas.
1. Aplicar filtro para obtener formas de imagen.
1. Guarde el Visio diagram resultante en el espacio local.
#### **Reemplazar una muestra de programación de forma de imagen**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **Importar imagen de mapa de bits como forma Visio**
Aspose.Diagram for .NET API ahora permite a los desarrolladores importar una imagen de mapa de bits como una forma Microsoft Visio.
### **Insert a BMP Image in Visio**
El código de los ejemplos siguientes muestra cómo:

1. Crea un diagram.
1. Obtener Visio página
1. Importe una imagen de mapa de bits como una forma Visio
1. Guarda el diagram.
#### **Insert a BMP Image Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
## **Convertir área especificada de la página Visio en una imagen**
Con Aspose.Diagram for .NET API, los desarrolladores pueden definir un área con coordenadas XY, ancho y alto, y luego convertir esta área a un formato de imagen compatible.
### **Convierta el área de dibujo Visio en una imagen**
El código de los ejemplos siguientes muestra cómo:

1. Cargue un dibujo Visio existente
1. Definir el área del rectángulo
1. Convertir el área especificada en una imagen

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
