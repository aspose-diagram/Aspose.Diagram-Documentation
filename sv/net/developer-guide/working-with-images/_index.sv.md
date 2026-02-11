---
title: Arbeta med bilder
type: docs
weight: 60
url: /sv/net/working-with-images/
description: Det här avsnittet förklarar hur man infogar eller hämtar en bild från en visio-sida med Aspose.Diagram.
---
## **Extrahera alla bilder från en Visio-sida**
I Microsoft Visio är sidorna antingen förgrunds- eller bakgrundssidor. Du kan extrahera bilder från en viss sida i en Visio-fil.
### **Extrahera bilder**
Sidklassobjektet representerar ritytan på en förgrundssida eller en bakgrundssida. Shapes-egenskapen som exponeras av klassen Diagram stöder en samling Aspose.Diagram.Shape-objekt. Den här egenskapen kan användas för att extrahera alla bilder från en viss sida.
#### **Extrahera bilder Programmeringsexempel**
Följande kodbit extraherar alla bilder från en viss Visio-sida.


{{< highlight csharp >}}
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

## **Få ikoner av olika Visio former**
Aspose.Diagram for .NET API tillåter nu utvecklare att få ikoner av olika Visio former.
### **Få formikonen**
Koden i exemplen nedan visar hur man:

1. Ladda en befintlig diagram eller stencil.
1. Få mästare efter dess index
1. Få master ikon.
1. Spara ikonen till det lokala utrymmet.
#### **Få ikoner programmering exempel**

{{< highlight csharp >}}
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

## **Byt ut en bildform på Visio Diagram**
Aspose.Diagram for .NET API låter utvecklare komma åt och ersätta tillgängliga bildformer i Visio diagram.
### **Byta ut en bildform**
Koden i exemplen nedan visar hur man:

1. Ladda ett befintligt diagram.
1. Iterera genom de selektiva sidformerna.
1. Använd filter för att få bildformer.
1. Spara resulterande Visio diagram till det lokala utrymmet.
#### **Byt ut ett bildformsprogrammeringsprov**

{{< highlight csharp >}}
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

## **Importera bitmappsbild som en Visio-form**
Aspose.Diagram for .NET API tillåter nu utvecklare att importera en bitmappsbild som en Microsoft Visio form.
### **Infoga en BMP-bild i Visio**
Koden i exemplen nedan visar hur man:

1. Skapa ett diagram.
1. Skaffa Visio sida
1. Importera en bitmappsbild som en Visio-form
1. Spara diagram.
#### **Infoga ett BMP bildprogrammeringsexempel**

{{< highlight csharp >}}
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

## **Konvertera specificerat område på Visio-sidan till en bild**
Med Aspose.Diagram for .NET API kan utvecklare definiera ett område med XY-koordinater, bredd och höjd och sedan konvertera detta område till ett bildformat som stöds.
### **Konvertera Visio rityta till en bild**
Koden i exemplen nedan visar hur man:

1. Ladda en befintlig Visio-ritning
1. Definiera rektangelområdet
1. Konvertera specificerat område till en bild

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
