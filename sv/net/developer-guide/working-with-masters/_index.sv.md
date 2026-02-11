---
title: Arbeta med Masters
type: docs
weight: 70
url: /sv/net/working-with-masters/
description: Det här avsnittet förklarar hur man lägger till master eller får masterinformation med Aspose.Diagram.
---
## **Hämtar masterinformation**
En formmästare är ett annat namn för en Visio stencil. Med Aspose.Diagram är det möjligt att hämta information om sidor, kopplingar och även masters. Den här artikeln förklarar hur du får ID och namn från en diagram.

 De[Bemästra](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objekt representerar en[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objektets master i en diagram. Masters-egenskapen, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Master-objekt. Den här egenskapen kan användas för att hämta befälhavarnas information, det vill säga master-ID och namn. Använd egenskapen Page.Shapes för att avgöra vilken form som har ärvts av masterformen.
### **Hämtar Master Information Programmeringsexempel**
Följande kodbit hämtar masterinformationen från en diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Master();

// Call a Diagram class constructor to load the VDX diagram
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveMasterInfo.vdx");

foreach (Aspose.Diagram.Master master in vdxDiagram.Masters)
{
    // Display information about the masters
    Console.WriteLine("\nMaster ID : " + master.ID);
    Console.WriteLine("Master Name : " + master.Name);
}
            
Console.ReadLine();

{{< /highlight >}}
```
## **Lägg till Master från Stencil of Shapes**
En stencil är en samling former som är associerade med en viss mall Microsoft Office Visio. Med Aspose.Diagram är det möjligt att lägga till valfri formmaster till en ritning från en stencil.
### **Lägg till Master**
 De[Bemästra](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objekt representerar en[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objektets master i en diagram. AddMaster-metoden, exponerad av klassen Diagram, tillåter att lägga till en master från en stencil. Den erbjuder följande fyra sätt:

- Stencilfilsökväg och master-ID.
- Stencilfilsökväg och huvudnamn.
- Stencilfilström och master-ID.
- Stencilfilström och huvudnamn.
- Lägg till master till diagram från källan diagram
#### **Lägg till masterprogrammeringsexempel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Master();

// Load diagram
Diagram diagram = new Diagram();

// Load stencil to a stream
string templateFileName = dataDir + "NetApp-FAS-series.vss";
Stream stream = new FileStream(templateFileName, FileMode.Open);

// Add master with stencil file path and master id
string masterName = "FAS80xx rear empty";
diagram.AddMaster(templateFileName, 2);

// Add master with stencil file path and master name
diagram.AddMaster(templateFileName, masterName);

// Add master with stencil file stream and master id
diagram.AddMaster(stream, 2);

// Adds master to diagram from source diagram
Diagram src = new Diagram(templateFileName);
diagram.AddMaster(src, masterName);

// Add master with stencil file stream and master id
diagram.AddMaster(stream, masterName);

// Adds shape with defined PinX and PinY.
diagram.AddShape(2.0, 2.0, masterName, 0);
diagram.AddShape(6.0, 6.0, masterName, 0);

// Adds shape with defined PinX,PinY,Width and Height.
diagram.AddShape(7.0, 3.0, 1.5, 1.5, masterName, 0);

{{< /highlight >}}
```
## **Skapa Master från grunden**
 Aspose.Diagram API gör det möjligt att skapa en[Bemästra](http://www.aspose.com/api/net/diagram/aspose.diagram/master) från grunden utan någon stencil, ritning eller mall. Utvecklare kan anpassa skapandet av Master. AddMaster-metoden, exponerad av klassen Diagram, tillåter att lägga till en master.
### **Skapa masterprogrammeringsexempel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public static void Run()
{            
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

    // Create a new template
    Diagram diagram = new Diagram();
    // Add master
    diagram.Masters.Add(CreateMaster(101, "Regular", dataDir + "aspose-logo.jpg"));
    // Save template
    diagram.Save(dataDir + "CreateMasterFromScratch_out.vtx", SaveFileFormat.VTX);           
}

// Create master
public static Master CreateMaster(int masterId, string name, string masterImage)
{
    // Set master properties
    Master master = new Master();
    master.ID = masterId;
    master.Name = name;
    master.IconSize = IconSizeValue.Normal;
    master.AlignName = AlignNameValue.AlignTextCenter;
    master.MatchByName = BOOL.True;
    master.IconUpdate = BOOL.True;
    master.UniqueID = Guid.NewGuid();
    master.BaseID = Guid.NewGuid();
    master.PatternFlags = 1;
    master.Hidden = BOOL.False;

    // Set master's shape properties
    Shape shape = new Shape();
    master.Shapes.Add(shape);

    double width = 0.5443889263424177;
    double height = 0.432916947568133;
    shape.ID = 5;
    shape.Type = TypeValue.Foreign;
    shape.XForm.PinX.Value = 0.2221944631712089;
    shape.XForm.PinY.Value = 0.1666458473784065;
    shape.XForm.Width.Value = width;
    shape.XForm.Height.Value = height;
    shape.XForm.LocPinX.Ufe.F = "Width*0.5";
    shape.XForm.LocPinY.Ufe.F = "Height*0.5";
    shape.XForm.ResizeMode.Value = 0;
    shape.TextXForm.TxtPinY.Ufe.F = "-TxtHeight/2";
    shape.TextXForm.TxtWidth.Ufe.F = "TEXTWIDTH(TheText)";
    shape.TextXForm.TxtHeight.Ufe.F = "TEXTHEIGHT(TheText, TxtWidth)";

    // Set connection properties
    Connection connection = new Connection();
    shape.Connections.Add(connection);

    connection.ID = 1;
    connection.NameU = "All";
    connection.X.Value = 0.22;
    connection.X.Ufe.F = "Width*0.5";
    connection.Y.Value = 0.16;
    connection.Y.Ufe.F = "Height*0.5";
    connection.DirX.Value = 0;
    connection.DirY.Value = 0;
    connection.Type.Value = 0;
    connection.AutoGen.Value = BOOL.False;
    connection.Prompt.Ufe.F = "No Formula";

    shape.ForeignData.ForeignType = ForeignType.Bitmap;
    shape.ForeignData.CompressionType = CompressionType.PNG;
    shape.ForeignData.Value = ReadImageFile(masterImage); // EncodedImage.getBytes();

    return master;
}
// Get image bytes
public static byte[] ReadImageFile(string imageLocation)
{
    byte[] imageData = null;
    FileInfo fileInfo = new FileInfo(imageLocation);
    long imageFileLength = fileInfo.Length;
    FileStream fs = new FileStream(imageLocation, FileMode.Open, FileAccess.Read);
    BinaryReader br = new BinaryReader(fs);
    imageData = br.ReadBytes((int)imageFileLength);
    return imageData;
}

{{< /highlight >}}
```
## **Skaffa en Master från filen Visio**
Ibland behöver utvecklare få detaljerna om en Visio ritnings master. Aspose.Diagram API stöder den här funktionen.

 Aspose.Diagram for .NET erbjuder[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)klass som representerar en Visio-ritning. Masters-egenskapen, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Master-objekt. Den här egenskapen kan användas för att hämta en viss masters detaljer. Klassen MasterCollection exponerar metoderna GetMasterByName och GetMaster som kan anropas för att få ett Master-objekt.
### **Få ett huvudobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters-klassens GetMaster-metod.
#### **Master Object by ID-programmeringsexempel**
Följande exempel visar hur man får en master genom ID från en Visio-ritning.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Master();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "RetrieveMasterInfo.vdx");

// Set master id
int masterid = 2;
// Get master object by id
Master master = diagram.Masters.GetMaster(masterid);

Console.WriteLine("Master ID : " + master.ID);
Console.WriteLine("Master Name : " + master.Name);
Console.WriteLine("Master Name : " + master.UniqueID);

{{< /highlight >}}
```
### **Få ett huvudobjekt med namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters-klassens GetMasterByName-metod.
#### **Master Object by Name Programmeringsexempel**
Följande exempel visar hur man hämtar ett huvudobjekt med namn från en Visio-ritning.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Master();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Set master name
string masterName = "Circle";
// Get master object by name
Master master = diagram.Masters.GetMasterByName(masterName);

Console.WriteLine("Master ID : " + master.ID);
Console.WriteLine("Master Name : " + master.Name);
Console.WriteLine("Master Name : " + master.UniqueID);

{{< /highlight >}}
```
## **Kontrollera närvaron av en master i Visio-ritningen**
Aspose.Diagram API stöder kontroll av närvaron av en master i en Visio-ritning. Med MasterCollection-egenskapen kan utvecklare kontrollera om en master är närvarande med sitt namn eller ID.

 Aspose.Diagram for .NET erbjuder[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass som representerar en Visio-ritning. Masters-egenskapen, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Master-objekt. Den här egenskapen kan användas för att kontrollera förekomsten av en viss master. Klassen MasterCollection exponerar IsExist-metoden som kan anropas med masternamnet eller ID-parametern.
### **Kontrollera en masternärvaro med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters class' IsExist-metod.
#### **Mästarnärvaro genom ID-programmeringsexempel**
Följande exempel visar hur man kontrollerar närvaron av en master genom ID i en Visio-ritning.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Master();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Check master by id
bool isPresent = diagram.Masters.IsExist(2);

Console.WriteLine("Master Presence : " + isPresent);

{{< /highlight >}}
```
### **Kontrollera en mästarnärvaro efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters class' IsExist-metod.
#### **Master Presence by Name Programmeringsexempel**
Följande exempel visar hur man kontrollerar en masternärvaro med namn från Visio-ritningen.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Master();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Set master name
string masterName = "VNXe3100 Storage Processor Rear";
// Check master object by name
bool isPresent = diagram.Masters.IsExist(masterName);

Console.WriteLine("Master Presence : " + isPresent);

{{< /highlight >}}
```
