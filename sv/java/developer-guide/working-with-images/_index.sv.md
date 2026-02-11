---
title: Arbeta med bilder
type: docs
weight: 70
url: /sv/java/working-with-images/
---
## **Extrahera alla bilder från en Visio-sida**
I Microsoft Visio är sidorna antingen förgrunds- eller bakgrundssidor. Du kan extrahera bilder från en viss sida i en Visio-fil.
### **Extrahera bilder**
Sidklassobjektet representerar ritytan på en förgrundssida eller en bakgrundssida. Shapes-egenskapen som exponeras av klassen Diagram stöder en samling Aspose.Diagram.Shape-objekt. Den här egenskapen kan användas för att extrahera alla bilder från en viss sida.
#### **Extrahera bilder Programmeringsexempel**
Följande kodbit extraherar alla bilder från en viss Visio-sida.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
## **Få ikoner av olika Visio former**
Aspose.Diagram for Java API tillåter nu utvecklare att få ikoner av olika Visio former.
### **Få formikonen**
Koden i exemplen nedan visar hur man:

1. Ladda en befintlig diagram eller stencil.
1. Få mästare efter dess index
1. Få master ikon.
1. Spara ikonen till det lokala utrymmet.
#### **Få ikoner programmering exempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetShapeIcon.class);  
// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// get master
Master master = stencil.getMasters().getMasterByName("Triangle");
// get byte array
byte[] bytes = master.getIcon();
// create an image file
FileOutputStream fos = new FileOutputStream(dataDir + "MasterIcon_Out.png");
// write byte array of the image
fos.write(bytes);
// close array
fos.close();

{{< /highlight >}}
```
## **Byt ut en bildform på Visio Diagram**
Aspose.Diagram for Java API låter utvecklare komma åt och ersätta tillgängliga bildformer i Visio diagram.
### **Byta ut en bildform**
Koden i exemplen nedan visar hur man:

1. Ladda ett befintligt diagram.
1. Iterera genom de selektiva sidformerna.
1. Använd filter för att få bildformer.
1. Spara resulterande Visio diagram till det lokala utrymmet.
#### **Byt ut ett bildformsprogrammeringsprov**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReplaceShapePicture.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
        
// convert image into bytes array       
File fi = new File(dataDir + "Picture.png");
byte[] fileContent = Files.readAllBytes(fi.toPath());
		
// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        //replace picture shape
    	shape.getForeignData().setValue(fileContent);
    }
}

// save diagram
diagram.save(dataDir + "ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Importera bitmappsbild som en Visio-form**
Aspose.Diagram for Java API tillåter nu utvecklare att importera en bitmappsbild som en Microsoft Visio form.
### **Infoga en BMP-bild i Visio**
Koden i exemplen nedan visar hur man:

1. Skapa ett diagram.
1. Skaffa Visio sida
1. Importera en bitmappsbild som en Visio-form
1. Spara diagram.
#### **Infoga ett BMP bildprogrammeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
