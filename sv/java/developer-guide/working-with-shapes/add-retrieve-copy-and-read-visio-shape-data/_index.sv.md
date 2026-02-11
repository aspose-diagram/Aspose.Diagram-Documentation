---
title: Lägg till, hämta, kopiera och läs Visio Shape Data
type: docs
weight: 10
url: /sv/java/add-retrieve-copy-and-read-visio-shape-data/
description: Det här avsnittet förklarar hur du lägger till en form, ställer in formens egenskap eller kopierar en form med Aspose.Diagram.
---
## **Lägger till en ny form i Visio**
Aspose.Diagram for Java låter dig manipulera Microsoft Visio diagram på olika sätt. En av sakerna du kan göra är att lägga till nya former till ett diagram. Aspose.Diagram for Java låter dig lägga till en ny form till en diagram. Den tillagda formen kan också anpassas med Aspose.Diagram for Java.

Det här avsnittet beskriver hur du lägger till en ny rektangelform till en diagram.

Använd Aspose.Diagram for Java API för att skapa nya former och lägg sedan till dessa former i en diagram:s formsamling.

Så här lägger du till en ny form:

1. **Hitta sidan** - Varje Visio diagram innehåller en samling sidor. Utvecklare kan hämta sidan efter sid-ID eller namn och lagra den önskade sidan i[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)klassobjekt.
1. **Lägg till den kräver Master of a Shape** - Varje Visio diagram innehåller en samling mästare. Utvecklare kan lägga till en Master (med ID eller Namn) från den befintliga stencilfilen (via direkt sökväg eller filström).
1. **Lägg till form i Visio diagram** - Utvecklare kan placera en ny form i Visio diagram efter sidindex (med början från 0), masternamn, PinX, PinY, höjd (valfritt) och bredd (valfritt).
1. **Ställ in formegenskaper** - AddShape-metoden för klassen Diagram returnerar form-ID. Utvecklare kan hämta form från en Visio diagram genom att använda detta ID och sedan ställa in dess egenskaper, t.ex. färg, position, justering och text.

|<p>**Ingången diagram** </p><p>![todo:image_alt_text](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**diagram med en form tillagd** </p><p>![todo:image_alt_text](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Lägg till programmeringsexempel**
Kodavsnittet nedan visar hur du gör varje steg.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddingNewShape.class);  
//Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-2");

// Add master with stencil file path and master id
String masterName = "Rectangle";
// Add master with stencil file path and master name
diagram.addMaster(dataDir + "Basic Shapes.vss", masterName);
            
// page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
//Add a new rectangle shape
long rectangleId = diagram.addShape(pinX, pinY, width, height, masterName, PageIndex);
            
// set shape properties 
Shape rectangle = page.getShapes().getShape(rectangleId);
rectangle.getXForm().getPinX().setValue(5);
rectangle.getXForm().getPinY().setValue(5);
rectangle.setType(TypeValue.SHAPE);
rectangle.getText().getValue().add(new Txt("Aspose Diagram"));
rectangle.setTextStyle(diagram.getStyleSheets().get(3));
rectangle.getLine().getLineColor().setValue("#ff0000");
rectangle.getLine().getLineWeight().setValue(0.03);
rectangle.getLine().getRounding().setValue(0.1);
rectangle.getFill().getFillBkgnd().setValue("#ff00ff");
rectangle.getFill().getFillForegnd().setValue("#ebf8df");

diagram.save(dataDir + "AddShape_Out.vsdx", SaveFileFormat.VSDX);
System.out.println("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}}
## **Hämta forminformation**
[Arbeta med diagram](/diagram/sv/java/working-with-diagrams/)förklarar hur man skapar diagram, lägger till former och kopplingar och sedan hur man hämtar information om diagram element som t.ex.[sidor](/diagram/sv/java/retrieve-get-copy-and-insert-a-page/), [mästare](https://docs.aspose.com/diagram/java/working-with-masters/), [kontakter](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) och[teckensnitt](https://reference.aspose.com/diagram/java/com.aspose.diagram/FontCollection). Den här artikeln tittar på hur du hämtar information om former i en diagram.

Varje form i en diagram har ett ID och ett namn. ID:t är viktigt vid programmering med Visio: det är huvudmetoden för att komma åt en form. Varje form behåller också information om vilken master (stencil) den är gjord av.

 A[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) är ett objekt i en Visio-ritning. Shapes-egenskapen, exponerad av klassen Page, stöder en samling Aspose.Diagram.Shape-objekt. Egenskapen Shapes kan användas för att hämta information om en form.

I konsolfönstret nedan kan du till exempel se informationsutmatning för en diagram som innehöll fyra former: två terminatorer, en process och en dynamisk kontakt. Var och en har ett unikt ID samt namnet på huvudformen (stencil).

|**Ett konsolfönster som visar forminformation**|
|:- |
|![todo:image_alt_text](add-retrieve-copy-and-read-visio-shape-data_3.png)|
För att hämta Visio sidinformation:

1. Laddar en diagram.
1. Ställer upp en foreach loop för att gå igenom alla former i diagram.
1. Visar forminformation.
### **Hämta programmeringsexempel**
Följande kodbit hämtar forminformationen från en Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveShapeInfo.class);

//Load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveShapeInfo.vsd");

for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    //Display information about the shapes
    System.out.println("\nShape ID : " + shape.getID());
    System.out.println("Name : " + shape.getName());
    System.out.println("Master Shape : " + shape.getMaster().getName());
}

{{< /highlight >}}


## **Kopiera former från en befintlig Visio**
Aspose.Diagram for Java API tillåter utvecklare att kopiera former från källsidan Visio till den nya sidan Visio diagram. Det stöder också kopiering av gruppformer. Den här artikeln beskriver hur du kopierar alla former från sidan källan diagram.

För att kopiera former bör utvecklare också kopiera källteman för PageSheet och källkod Visio för att bevara formfyllningsstil och andra formateringsegenskaper.

Detta exempel fungerar enligt följande:

1. Ladda en källa Visio.
1. Initiera ett nytt Visio
1. Lägg till masters och teman från källan Visio.
1. Hämta sida från källan Visio.
1. Kopiera dess PageSheet till den nya Visio-sidan.
1. Iterera genom formerna på källsidan Visio.
1. Ställ in dess nya id och lägg till den nya sidan Visio.
1. Spara det nya Visio i den lokala lagringen.
### **Kopiera programmeringsexempel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyShape.class); 
// load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
        
// initialize a new Visio
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.getMasters();
for (Master master : (Iterable<Master>) originalMasters)
    newDiagram.addMaster(srcVisio, master.getName());

// get the page object from the original diagram
Page SrcPage = srcVisio.getPages().getPage("Page-1");
// copy themes from the source diagram
newDiagram.copyTheme(srcVisio);
// copy pagesheet of the source Visio page
newDiagram.getPages().get(0).getPageSheet().copy(SrcPage.getPageSheet());

// copy shapes from the source Visio page
for (Shape shape :(Iterable<Shape>) SrcPage.getShapes())
{
    newDiagram.getPages().get(0).getShapes().add(shape);
}
// save the new Visio
newDiagram.save(dataDir + "CopyShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



{{% alert color="primary" %}}

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}}
## **Kopiera en Visio Shape till en annan Shape-instans**
Kopieringsmetoden för Shape-klassen kräver en forminstans för att klona.

## **Läser Visio Shape Data**
 Rekvisitasamlingen exponerad av[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) klass stöder[Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/prop) objekt. Egenskapen kan användas för att läsa en forms data (anpassade egenskaper).
### **Läs alla formegenskaper**
Så här identifierar du anpassade egenskaper i Microsoft Visio:

1. I en diagram högerklickar du på en form.
1.  Välj**Data** , då**Formdata** från menyn.
 Alla befintliga egenskaper listas i dialogrutan.

|**En forms data, som ses i Microsoft Visio.**|** |
|:- |:- |
|![todo:image_alt_text](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**Ett konsolfönster som visar formdatautmatningen.**|** |
|:- |:- |
|![todo:image_alt_text](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **Läs programmeringsexempel**
Kodavsnitten nedan läser formdata (anpassade egenskaper).


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadAllShapeProps.class);  

// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        for (Prop property :(Iterable<Prop>) shape.getProps())
        {
            System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
        }
        break;
    }
}

{{< /highlight >}}


### **Läs en Shape Property efter namn**
Kodavsnittet nedan läser en formegenskap efter namn (anpassad egenskap).
#### **Läs efter namn Programmeringsexempel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadShapePropByName.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        Prop property = shape.getProps().getProp("Name1");
        System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
    }
}

{{< /highlight >}}


## **Använd anslutningsindex för att koppla samman former**
Aspose.Diagram for Java API tillåter redan utvecklare att lägga till nya anslutningspunkter på formen, och utvecklare kan nu ansluta former med hjälp av anslutningsindex.
### **Använd anslutningsindex för att koppla samman former**
ConnectShapesViaConnectorIndex-medlemmen exponerad av[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)klass kan användas för att koppla samman former med hjälp av anslutningsindex.

1. Initiera en ny ritning.
1. Placera fyra rektangelformer
1. Lägg till ytterligare två anslutningspunkter så att det blir tre anslutningspunkter på den nedre gränslinjen
1. Anslut den första formen från varje nedre anslutning till andra tre rektangelformer från Top med dynamiska kopplingar
1. Spara ritningen
#### **Använd anslutningsindex för att koppla samman former Programmeringsexempel**
Använd följande kod i din Java-applikation för att ansluta former med anslutningsindex med Aspose.Diagram for Java API.

## **Hämta den överordnade formen för en underform**
Aspose.Diagram for Java tillåter utvecklare att hämta den överordnade formen för en underform.
### **Skaffa föräldraformen**
De[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)class erbjuder ParentShape-egenskapen för att hämta den överordnade formen.
#### **Skaffa programmet Parent Shape-programmering**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
		
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
Shape parentShape = shape.getParentShape();
System.out.println("Parent Shape's Properties:");
System.out.println("Shape ID: " + parentShape.getID());
System.out.println("Shape Name: " + parentShape.getName());
System.out.println("Shape Type: " + parentShape.getType());
{{< /highlight >}}


