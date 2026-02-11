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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Load memory stream into bitmap object
            System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

            // Save bmp here
            bitmap.Save(dataDir + "ExtractAllImages" + shape.ID + "_out.bmp");
        }
    }
}

{{< /highlight >}}
```
## **Obtener íconos de varias formas Visio**
Aspose.Diagram for .NET API ahora permite a los desarrolladores obtener íconos de varias Visio formas.
### **Obtener el icono de forma**
El código de los ejemplos siguientes muestra cómo:

1. Cargue un diagram o plantilla existente.
1. Obtener maestro por su índice
1. Obtener icono maestro.
1. Guardar icono en el espacio local.
#### **Muestra de Programación de Obtener Iconos**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// Get master
Master master = stencil.Masters.GetMaster(1);

using (System.IO.MemoryStream stream = new System.IO.MemoryStream(master.Icon))
{
    // Load memory stream into bitmap object
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);
    // Save as png format
    bitmap.Save(dataDir + "MasterIcon_out.png", System.Drawing.Imaging.ImageFormat.Png);
}

{{< /highlight >}}
```
## **Reemplace una forma de imagen del Visio Diagram**
Aspose.Diagram for .NET API permite a los desarrolladores acceder y reemplazar formas de imagen disponibles en Visio diagram.
### **Sustitución de una forma de imagen**
El código de los ejemplos siguientes muestra cómo:

1. Cargue un diagram existente.
1. Iterar a través de las formas de página selectivas.
1. Aplicar filtro para obtener formas de imagen.
1. Guarde el Visio diagram resultante en el espacio local.
#### **Reemplazar una muestra de programación de forma de imagen**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
// Convert image into bytes array
byte[] imageBytes = File.ReadAllBytes(dataDir + "Picture.png");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Replace picture shape
            shape.ForeignData.Value = imageBytes;
        }
    }
}

// Save diagram
diagram.Save(dataDir + "ReplaceShapePicture_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Importar imagen de mapa de bits como forma Visio**
Aspose.Diagram for .NET API ahora permite a los desarrolladores importar una imagen de mapa de bits como una forma Microsoft Visio.
### **Insert a BMP Image in Visio**
El código de los ejemplos siguientes muestra cómo:

1. Crea un diagram.
1. Obtener Visio página
1. Importe una imagen de mapa de bits como una forma Visio
1. Guarda el diagram.
#### **Insert a BMP Image Programming Sample**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Create a new diagram
Diagram diagram = new Diagram();

// Get page object by index
Page page0 = diagram.Pages[0];
// Set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import Bitmap image as Visio shape
page0.AddShape(pinX, pinY, width, hieght, new FileStream(dataDir + "image.bmp", FileMode.OpenOrCreate));

// Save Visio diagram
diagram.Save(dataDir + "InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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
