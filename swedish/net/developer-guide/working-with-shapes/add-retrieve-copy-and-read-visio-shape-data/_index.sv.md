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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-AddingNewShape-AddingNewShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CopyShape-CopyShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadAllShapeProps-ReadAllShapeProps.cs" >}}
### **Läs en Shape Property efter namn**
Kodavsnittet nedan läser en formegenskap efter namn (anpassad egenskap).
#### **Läs efter namn Programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadShapePropByName-ReadShapePropByName.cs" >}}
### **Läs InheritProps of Shape**
Kodavsnittet nedan läser InheritProps av en form.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-InheritProps-InheritProps.cs" >}}
## **Lägg till och anslut Visio Former**
 Aspose.Diagram for .NET låter dig lägga till anpassade former och ansluta dem i[diagram du skapar](https://products.aspose.com/diagram/net/).
### **Lägga till och ansluta former**
Koden i exemplen nedan visar hur man:

1. Skapa ett diagram.
1. Lägg till och anpassa former (rektangel, stjärna, hexagon).
1. Anslut stjärnan och hexagonformerna till rektangeln.
1. Spara diagram.
#### **Lägga till och ansluta former Programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Technical-Articles-AddConnectShapes-AddConnectShapes.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.cs" >}}
