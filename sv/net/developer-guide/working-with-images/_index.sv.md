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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **Få ikoner av olika Visio former**
Aspose.Diagram for .NET API tillåter nu utvecklare att få ikoner av olika Visio former.
### **Få formikonen**
Koden i exemplen nedan visar hur man:

1. Ladda en befintlig diagram eller stencil.
1. Få mästare efter dess index
1. Få master ikon.
1. Spara ikonen till det lokala utrymmet.
#### **Få ikoner programmering exempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **Byt ut en bildform på Visio Diagram**
Aspose.Diagram for .NET API låter utvecklare komma åt och ersätta tillgängliga bildformer i Visio diagram.
### **Byta ut en bildform**
Koden i exemplen nedan visar hur man:

1. Ladda ett befintligt diagram.
1. Iterera genom de selektiva sidformerna.
1. Använd filter för att få bildformer.
1. Spara resulterande Visio diagram till det lokala utrymmet.
#### **Byt ut ett bildformsprogrammeringsprov**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **Importera bitmappsbild som en Visio-form**
Aspose.Diagram for .NET API tillåter nu utvecklare att importera en bitmappsbild som en Microsoft Visio form.
### **Infoga en BMP-bild i Visio**
Koden i exemplen nedan visar hur man:

1. Skapa ett diagram.
1. Skaffa Visio sida
1. Importera en bitmappsbild som en Visio-form
1. Spara diagram.
#### **Infoga ett BMP bildprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
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
