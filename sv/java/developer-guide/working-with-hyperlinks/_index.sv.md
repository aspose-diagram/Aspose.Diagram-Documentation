---
title: Arbeta med hyperlänkar
type: docs
weight: 110
url: /sv/java/working-with-hyperlinks/
---
## **Lägg till hyperlänk till en Visio-form**
Det är ett enkelt sätt att lägga till hyperlänkar till Microsoft Visio form dynamiskt.

På flersidiga Visio ritningar kan hyperlänkar flytta dig från en sida till en annan. Du kan också länka din ritning till en webbsida eller en fil på ditt system.

Dessa egenskaper exponeras av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) klass stöder[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink) objekt. Add-metoden kan användas för att lägga till en forms hyperlänkdata.

Så här identifierar du fastigheter i Microsoft Visio:

1. I en diagram högerklickar du på en form.
1.  Välj**Hyperlänk**.
1. Ange befintliga egenskaper
1.  Tryck**OK** knapp

**En forms hyperlänksdata, som ses i Microsoft Visio**

![todo:image_alt_text](working-with-hyperlinks_1.png)

Kodavsnitten nedan lägger till forms hyperlänkdata.
### **Lägg till hyperlänksprogrammeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Hämta hyperlänkdata för Visio-formerna**
 Det är möjligt att få en forms hyperlänkdata på liknande sätt som du[läser Visio formdata]().

Utvecklare kan hämta alla hyperlänkar från en Visio-form på samma sätt som de[läs Visio formdata]() använder sig av[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

I flersidiga Visio-ritningar kan hyperlänkar flytta dig från en sida till en annan. Du kan också länka din ritning till en webbsida eller en fil på ditt system.

Dessa egenskaper exponeras av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) klass stöder[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)objekt. Egenskapen kan användas för att läsa en forms hyperlänkdata.

Så här identifierar du fastigheter i Microsoft Visio:

1. I en diagram högerklickar du på en form.
1.  Välj**Hyperlänk.**
 Alla befintliga egenskaper listas i dialogrutan.

**En forms hyperlänksdata, som ses i Microsoft Visio**

![todo:image_alt_text](working-with-hyperlinks_2.png)

**Ett konsolfönster som visar formdatautmatningen**

![todo:image_alt_text](working-with-hyperlinks_3.png)

Kodavsnitten nedan läser shapes hyperlänkdata.
### **Få hyperlänksprogrammeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}
```
