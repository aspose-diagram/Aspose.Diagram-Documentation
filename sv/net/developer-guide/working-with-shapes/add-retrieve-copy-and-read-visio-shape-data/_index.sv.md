---
title: Lägg till, hämta, kopiera och läs Visio Shape Data
type: docs
weight: 10
url: /sv/net/add-retrieve-copy-and-read-visio-shape-data/
description: Det här avsnittet förklarar hur du lägger till en form, ställer in formens egenskap eller kopierar en form med Aspose.Diagram.
---
## **Lägger till en ny form i Visio**
Aspose.Diagram for .NET låter dig manipulera Microsoft Visio diagram på olika sätt. En av sakerna du kan göra är att lägga till nya former till ett diagram. Aspose.Diagram for .NET låter dig lägga till en ny form till en diagram. Den tillagda formen kan också anpassas med Aspose.Diagram for .NET.

Det här avsnittet beskriver hur du lägger till en ny rektangelform till en diagram.

Använd Aspose.Diagram for .NET API för att skapa nya former och lägg sedan till dessa former i en diagram:s formsamling.

Så här lägger du till en ny form:

1. **Hitta sidan** - Varje Visio diagram innehåller en samling sidor. Utvecklare kan hämta sidan efter sid-ID eller namn och lagra den önskade sidan i[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page)klassobjekt.
1. **Lägg till den kräver Master of a Shape** - Varje Visio diagram innehåller en samling mästare. Utvecklare kan lägga till en Master (med ID eller Namn) från den befintliga stencilfilen (via direkt sökväg eller filström).
1. **Lägg till form i Visio diagram** - Utvecklare kan placera en ny form i Visio diagram efter sidindex (med början från 0), masternamn, PinX, PinY, höjd (valfritt) och bredd (valfritt).
1. **Ställ in formegenskaper** - AddShape-metoden för klassen Diagram returnerar form-ID. Utvecklare kan hämta form från en Visio diagram genom att använda detta ID och sedan ställa in dess egenskaper, t.ex. färg, position, justering och text.

|<p>**Ingången diagram** </p><p>![todo:image_alt_text](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**diagram med en form tillagd** </p><p>![todo:image_alt_text](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Lägg till programmeringsexempel**
Kodavsnittet nedan visar hur du gör varje steg.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);
            
// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);
            
// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));
rectangle.TextStyle = diagram.StyleSheets[3];
rectangle.Line.LineColor.Value = "#ff0000";
rectangle.Line.LineWeight.Value = 0.03;
rectangle.Line.Rounding.Value = 0.1;
rectangle.Fill.FillBkgnd.Value = "#ff00ff";
rectangle.Fill.FillForegnd.Value = "#ebf8df";

diagram.Save(dataDir + "AddShape_out.vsdx", SaveFileFormat.VSDX);
Console.WriteLine("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}}
## **Hämta forminformation**
[Arbeta med diagram](/diagram/sv/net/working-with-diagrams/)förklarar hur man skapar diagram, lägger till former och kopplingar och sedan hur man hämtar information om diagram element som t.ex.[sidor](/diagram/sv/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [mästare](https://docs.aspose.com/diagram/net/working-with-masters/), [kontakter](/diagram/sv/net/retrieving-connector-information/) och[teckensnitt](/diagram/sv/net/retrieving-font-information/). Den här artikeln tittar på hur du hämtar information om former i en diagram.

Varje form i en diagram har ett ID och ett namn. ID:t är viktigt vid programmering med Visio: det är huvudmetoden för att komma åt en form. Varje form behåller också information om vilken master (stencil) den är gjord av.

 A[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) är ett objekt i en Visio-ritning. Shapes-egenskapen, exponerad av klassen Page, stöder en samling Aspose.Diagram.Shape-objekt. Egenskapen Shapes kan användas för att hämta information om en form.

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");

foreach (Aspose.Diagram.Shape shape in vsdDiagram.Pages[0].Shapes)
{
    // Display information about the shapes
    Console.WriteLine("\nShape ID : " + shape.ID);
    Console.WriteLine("Name : " + shape.Name);
    Console.WriteLine("Master Shape : " + shape.Master.Name);
}

{{< /highlight >}}

## **Kopiera former från en befintlig Visio**
Aspose.Diagram for .NET API tillåter utvecklare att kopiera former från källsidan Visio till den nya sidan Visio diagram. Det stöder också kopiering av gruppformer. Den här artikeln beskriver hur du kopierar alla former från sidan källan diagram.

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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
            
// Initialize a new Visio
Diagram newDiagram = new Diagram();

// Add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.Masters;
foreach (Master master in originalMasters)
    newDiagram.AddMaster(srcVisio, master.Name);

// Get the page object from the original diagram
Aspose.Diagram.Page SrcPage = srcVisio.Pages.GetPage("Page-1");
// Copy themes from the source diagram
newDiagram.CopyTheme(srcVisio);
// Copy pagesheet of the source Visio page
newDiagram.Pages[0].PageSheet.Copy(SrcPage.PageSheet);

// Copy shapes from the source Visio page
foreach (Aspose.Diagram.Shape shape in SrcPage.Shapes)
{
    newDiagram.Pages[0].Shapes.Add(shape);
}
// Save the new Visio
newDiagram.Save(dataDir + "CopyShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}}

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}}
## **Kopiera en Visio Shape till en annan Shape-instans**
Kopieringsmetoden för Shape-klassen kräver en forminstans för att klona.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
## **Läser Visio Shape Data**
 Rekvisitasamlingen exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass stöder[Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) objekt. Egenskapen kan användas för att läsa en forms data (anpassade egenskaper).
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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        foreach (Prop property in shape.Props)
        {
            Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
        }
        break;
    }
}

{{< /highlight >}}

### **Läs en Shape Property efter namn**
Kodavsnittet nedan läser en formegenskap efter namn (anpassad egenskap).
#### **Läs efter namn Programmeringsexempel**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        Prop property = shape.Props.GetProp("Name1");
        Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
    }
}

{{< /highlight >}}

### **Läs InheritProps of Shape**
Kodavsnittet nedan läser InheritProps av en form.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    foreach (Aspose.Diagram.Prop prop in shape.InheritProps)
    {
        Console.WriteLine(prop.Name);
        Console.WriteLine(prop.Label.Value);
        Console.WriteLine(prop.Prompt.Value);
        Console.WriteLine(prop.Type.Value.ToString());
        Console.WriteLine(prop.Value.Val);
        Console.WriteLine(prop.Format.Value);
    }
}

{{< /highlight >}}

## **Lägg till och anslut Visio Former**
 Aspose.Diagram for .NET låter dig lägga till anpassade former och ansluta dem i[diagram du skapar](https://products.aspose.com/diagram/net/).
### **Lägga till och ansluta former**
Koden i exemplen nedan visar hur man:

1. Skapa ett diagram.
1. Lägg till och anpassa former (rektangel, stjärna, hexagon).
1. Anslut stjärnan och hexagonformerna till rektangeln.
1. Spara diagram.
#### **Lägga till och ansluta former Programmeringsexempel**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_TechnicalArticles();

// Set license (you can add 10 shapes without setting a license)
// License lic = new License();
// Lic.SetLicense(dataDir + "Aspose.Total.lic");

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
string visioStencil = dataDir + "AddConnectShapes.vss";

// Names of the masters present in the stencil
string rectangleMaster = @"Rectangle", starMaster = @"Star 7",
    hexagonMaster = @"Hexagon", connectorMaster = "Dynamic connector";

int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

// Create a new diagram
Diagram diagram = new Diagram(visioStencil);

// Add a new rectangle shape
long rectangleId = diagram.AddShape(
    pinX, pinY, width, height, rectangleMaster, pageNumber);

// Set the new shape's properties
Shape shape = diagram.Pages[pageNumber].Shapes.GetShape(rectangleId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));
shape.Name = "Rectangle1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "7";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "1";
shape.Fill.FillForegnd.Value = "3";
shape.Fill.FillPattern.Value = 31;

// Add a new star shape
pinX = 2.0;
pinY = 4.5;
long starId = diagram.AddShape(
    pinX, pinY, width, height, starMaster, pageNumber);

// Set the star shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(starId);
shape.Text.Value.Add(new Txt(@"Star text."));
shape.Name = "Star1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "#ff0000";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "#ff00ff";
shape.Fill.FillForegnd.Value = "#0000ff";
shape.Fill.FillPattern.Value = 31;

// Add a new hexagon shape
pinX = 7.0;
long hexagonId = diagram.AddShape(
    pinX, pinY, width, height, hexagonMaster, pageNumber);

// Set the hexagon shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(hexagonId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));
shape.Name = "Hexagon1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillPattern.Value = 31;

// Add master to dynamic connector from the stencil
diagram.AddMaster(visioStencil, connectorMaster);

// Connect rectangle and star shapes
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    starId, ConnectionPointPlace.Top, connecter1Id);

// Connect rectangle and hexagon shapes
Shape connector2 = new Shape();
long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    hexagonId, ConnectionPointPlace.Left, connecter2Id);

// Save the diagram
diagram.Save(dataDir + "AddConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Använd anslutningsindex för att koppla samman former**
Aspose.Diagram for .NET API tillåter redan utvecklare att lägga till nya anslutningspunkter på formen, och utvecklare kan nu ansluta former med hjälp av anslutningsindex.
### **Använd anslutningsindex för att koppla samman former**
ConnectShapesViaConnectorIndex-medlemmen exponerad av[Sida](https://reference.aspose.com/diagram/net/aspose.diagram/page)klass kan användas för att koppla samman former med hjälp av anslutningsindex. Följande kod visar hur man ansluter former:

1. Initiera en ny ritning.
1. Placera fyra rektangelformer
1. Lägg till ytterligare två anslutningspunkter så att det blir tre anslutningspunkter på den nedre gränslinjen
1. Anslut den första formen från varje nedre anslutning till andra tre rektangelformer från Top med dynamiska kopplingar
1. Spara ritningen
#### **Använd anslutningsindex för att koppla samman former Programmeringsexempel**
Använd följande kod i din .NET-applikation för att ansluta former med anslutningsindex med Aspose.Diagram for .NET API.

**C#**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Aspose.Diagram.Page page = diagram.Pages[0];

// add masters

string connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", rectangle);

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.AddShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.AddShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.AddShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.AddShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Aspose.Diagram.Shape shape1 = page.Shapes.GetShape(shape1_ID);

Aspose.Diagram.Shape shape2 = page.Shapes.GetShape(shape2_ID);

Aspose.Diagram.Shape shape3 = page.Shapes.GetShape(shape3_ID);

Aspose.Diagram.Shape shape4 = page.Shapes.GetShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.X.Ufe.F = "Width*0.33";

connection1.Y.Ufe.F = "Height*0";

Connection connection3 = new Connection();

connection3.X.Ufe.F = "Width*0.66";

connection3.Y.Ufe.F = "Height*0";

shape1.Connections.Add(connection1);

shape1.Connections.Add(connection3);



// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector2 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector3 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.AddShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 1, shape3.ID, 3, connecter2Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 7, shape4.ID, 3, connecter3Id);

// save drawing

diagram.Save(@"C:\temp\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Hämta den överordnade formen för en underform**
Aspose.Diagram for .NET tillåter utvecklare att hämta den överordnade formen för en underform.
### **Skaffa föräldraformen**
De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class erbjuder ParentShape-egenskapen för att hämta den överordnade formen.
#### **Skaffa programmet Parent Shape-programmering**

{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Shape parentShape = shape.ParentShape;
Console.WriteLine("Parent Shape's Properties:");
Console.WriteLine("Shape ID: " + parentShape.ID);
Console.WriteLine("Shape Name: " + parentShape.Name);
Console.WriteLine("Shape Type: " + parentShape.Type);
{{< /highlight >}}

