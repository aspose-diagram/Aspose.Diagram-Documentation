---
title: Arbeiten mit Meistern
type: docs
weight: 70
url: /de/net/working-with-masters/
description: In diesem Abschnitt wird erläutert, wie Sie mit Aspose.Diagram Master hinzufügen oder Masterinformationen abrufen.
---
## **Stammdaten abrufen**
Ein Shape-Master ist ein anderer Name für eine Visio-Schablone. Mit Aspose.Diagram können Informationen über Seiten, Konnektoren und auch Master abgerufen werden. Dieser Artikel erklärt, wie Sie die ID und den Namen von einer diagram erhalten.

 Das[Meister](http://www.aspose.com/api/net/diagram/aspose.diagram/master) Objekt repräsentiert a[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Master-Objekt in einem diagram. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um die Informationen des Masters abzurufen, d. h. die Master-ID und den Namen. Verwenden Sie die Page.Shapes-Eigenschaft, um zu bestimmen, welche Form von der Masterform geerbt wurde.
### **Programmierbeispiel für Stamminformationen abrufen**
Der folgende Codeabschnitt ruft die Masterinformationen von diagram ab.

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
## **Fügen Sie Master aus der Schablone der Formen hinzu**
Eine Schablone ist eine Sammlung von Formen, die einer bestimmten Microsoft Office Visio Vorlage zugeordnet sind. Mit Aspose.Diagram ist es möglich, beliebige Shape-Master zu einer Zeichnung aus einer Schablone hinzuzufügen.
### **Meister hinzufügen**
 Das[Meister](http://www.aspose.com/api/net/diagram/aspose.diagram/master) Objekt repräsentiert a[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Master des Objekts in einem diagram. Die Methode AddMaster, die von der Klasse Diagram verfügbar gemacht wird, ermöglicht das Hinzufügen eines Masters aus einer Schablone. Es bietet die folgenden vier Möglichkeiten:

- Pfad der Schablonendatei und Master-ID.
- Dateipfad und Mastername der Schablone.
- Schablonendateistream und Master-ID.
- Schablonendateistream und Mastername.
- Master zu diagram aus Quelle diagram hinzufügen
#### **Master-Programmierbeispiel hinzufügen**
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
## **Master von Grund auf neu erstellen**
 Aspose.Diagram API ermöglicht das Erstellen einer[Meister](http://www.aspose.com/api/net/diagram/aspose.diagram/master) von Grund auf ohne Schablone, Zeichnung oder Vorlage. Entwickler können die Erstellung von Master anpassen. Die Methode AddMaster, die von der Klasse Diagram verfügbar gemacht wird, ermöglicht das Hinzufügen eines Masters.
### **Master-Programmierbeispiel erstellen**
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
## **Holen Sie sich einen Master aus der Datei Visio**
Manchmal müssen Entwickler die Details des Masters einer Visio-Zeichnung abrufen. Die Aspose.Diagram API unterstützt diese Funktion.

 Aspose.Diagram for .NET bietet die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Klasse, die eine Visio-Zeichnung darstellt. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um die Details eines bestimmten Masters abzurufen. Die Klasse MasterCollection macht die Methoden GetMasterByName und GetMaster verfügbar, die aufgerufen werden können, um ein Master-Objekt abzurufen.
### **Abrufen eines Master-Objekts nach ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetMaster-Methode der Diagram.Masters-Klasse auf.
#### **Programmierbeispiel für Master-Objekt nach ID**
Das folgende Beispiel zeigt, wie Sie einen Master nach ID aus einer Visio-Zeichnung erhalten.

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
### **Abrufen eines Master-Objekts nach Namen**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetMasterByName-Methode der Diagram.Masters-Klasse auf.
#### **Master Object by Name Programmierbeispiel**
Das folgende Beispiel zeigt, wie Sie ein Master-Objekt anhand des Namens aus einer Visio-Zeichnung abrufen.

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
## **Überprüfen Sie das Vorhandensein eines Masters in der Visio-Zeichnung**
Die Aspose.Diagram API unterstützt die Überprüfung auf das Vorhandensein eines Masters in einer Visio-Zeichnung. Mit der MasterCollection-Eigenschaft können Entwickler anhand ihres Namens oder ihrer ID prüfen, ob ein Master vorhanden ist.

 Aspose.Diagram for .NET bietet die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um das Vorhandensein eines bestimmten Masters zu überprüfen. Die MasterCollection-Klasse macht die IsExist-Methode verfügbar, die mit dem Masternamen- oder ID-Parameter aufgerufen werden kann.
### **Überprüfen einer Master-Anwesenheit anhand der ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die IsExist-Methode der Diagram.Masters-Klasse auf.
#### **Master Presence by ID Programmierbeispiel**
Das folgende Beispiel zeigt, wie das Vorhandensein eines Masters anhand der ID in einer Visio-Zeichnung überprüft wird.

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
### **Überprüfen einer Master-Anwesenheit anhand des Namens**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die IsExist-Methode der Diagram.Masters-Klasse auf.
#### **Master Presence by Name Programmierbeispiel**
Das folgende Beispiel zeigt, wie eine Master-Anwesenheit anhand des Namens aus der Zeichnung Visio überprüft wird.

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
