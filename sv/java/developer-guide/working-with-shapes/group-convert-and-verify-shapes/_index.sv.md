---
title: Gruppera, konvertera och verifiera former
type: docs
weight: 50
url: /sv/java/group-convert-and-verify-shapes/
---
## **Gruppera flera former tillsammans i Visio-ritningen**
Aspose.Diagram API tillåter utvecklare att gruppera former för att flytta dem alla på en gång. Varje form i en grupp har en unik identitet och har sin egen uppsättning egenskaper. När vi ändrar formateringen av en grupp av former tilldelar den den nya egenskapen till varje form.
### **Hur man grupperar former**
Gruppmetoden som exponeras av klassen ShapeCollection kan användas för att gruppera former.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. initierade en uppsättning av formerna
1. få en viss form genom id.
1. få en annan speciell form genom id.
1. tilldela former till arrayen.
1. gruppera former genom att anropa gruppmetoden.
1. spara diagram
#### **Programmeringsexempel för gruppformer**
Använd följande kod i din Java-applikation för att gruppera former med Aspose.Diagram for Java API.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Konvertera en Visio Shape till andra filformat**
Aspose.Diagram for Java API tillåter utvecklare att konvertera en enda Visio-form till vilket annat filformat som helst. I den här artikeln tar vi bort alla andra Visio-former från sidan och anpassar sidinställningarna efter källans formstorlek.
### **Konvertera en viss Visio-form**
 Utvecklare kan konvertera en Visio-form till PDF, HTML, Image, SVG och SWF med[ange Visio sparalternativ]().
Den här exempelkoden fungerar enligt följande:

1. Ladda en källa Visio.
1. Skaffa en viss sida.
1. Ta bort bakgrundssidan.
1. Bygg en hashtabell med alla former som innehåller ID och namn.
1. Iterera genom hashtabellen
1. Ta bort alla former från Visio-sidan, utom den specifika.
1. Ställ in sidstorleken.
1. Spara sidan Visio i valfritt filformat som stöds.
#### **Konvertera formprogrammeringsexempel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}

### **Konvertera Visio Shape till PDF**
ToPdf-metoden för Shape-klassen gör det möjligt att konvertera en form till formatet PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Konvertera Visio Shape till HTML**
ToHTML-metoden för Shape-klassen gör det möjligt att konvertera en form till formatet HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}} 
## **Kontrollera om två Visio-former är anslutna eller limmade**
 Aspose.Diagram for Java API låter utvecklare verifiera att de två Visio-formerna är limmade eller sammankopplade. Tidigare har vi sett hur vi kan ansluta eller limma två former i dessa hjälpämnen:[Lägg till och anslut Visio Former](/diagram/sv/java/add-and-connect-visio-shapes/) och[Limma former inuti behållaren](/diagram/sv/java/working-with-shapes-gluing/).
### **Verifiering av de anslutna eller limmade formerna**
 De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class erbjuder egenskaperna IsGlued och IsConnected för att avgöra om två former är limmade eller sammankopplade.
#### **Verifiering av programmeringsprov för anslutna eller limmade former**
Följande kod verifierar om två former är sammankopplade eller limmade.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}

## **Verifiera om Visio-formen är i en grupp av former**
Aspose.Diagram for Java API tillåter utvecklare att verifiera att Visio-formen är i en grupp av former eller inte.
### **Verifiering av form i gruppen av former**
Klassen Shape erbjuder IsInGroup-egenskaper för att avgöra om formen Visio är i en gruppform.
#### **Verifiering av form i gruppen av formprogrammeringsexempel**
Följande kodbit verifierar om formen är i en gruppform.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}


{{% alert color="primary" %}} 

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}}
