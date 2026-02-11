---
title: Lavorare con i Maestri
type: docs
weight: 70
url: /it/net/working-with-masters/
description: Questa sezione spiega come aggiungere master o ottenere informazioni master con Aspose.Diagram.
---
## **Recupero delle informazioni sul master**
Uno shape master è un altro nome per uno stencil Visio. Con Aspose.Diagram è possibile recuperare informazioni su pagine, connettori e anche master. Questo articolo spiega come ottenere l'ID e il nome da uno diagram.

 Il[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'oggetto rappresenta a[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) master dell'oggetto in un oggetto diagram. La proprietà Masters, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Master. Questa proprietà può essere utilizzata per recuperare le informazioni sui master, ovvero l'ID e il nome del master. Utilizzare la proprietà Page.Shapes per determinare quale forma è stata ereditata dalla forma master.
### **Recupero del campione di programmazione delle informazioni principali**
Il seguente pezzo di codice recupera le informazioni master da un diagram.


{{< highlight csharp >}}
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

## **Aggiungi Master dallo Stencil di forme**
Uno stencil è una raccolta di forme associate a un particolare modello Microsoft Office Visio. Con Aspose.Diagram è possibile aggiungere qualsiasi modello di forma a un disegno da uno stencil.
### **Aggiungi Maestro**
 Il[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'oggetto rappresenta a[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) master dell'oggetto in un diagram. Il metodo AddMaster, esposto dalla classe Diagram, consente di aggiungere un master da uno stencil. Offre le seguenti quattro modalità:

- Percorso file stencil e ID master.
- Percorso file stencil e nome master.
- Flusso di file di stencil e ID principale.
- Flusso di file di stencil e nome principale.
- Aggiungi master a diagram dalla fonte diagram
#### **Aggiungi un esempio di programmazione principale**

{{< highlight csharp >}}
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

## **Crea Master da zero**
 Aspose.Diagram API permette di creare un[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) da zero senza alcuno stencil, disegno o modello. Gli sviluppatori possono personalizzare la creazione di Master. Il metodo AddMaster, esposto dalla classe Diagram, permette di aggiungere un master.
### **Crea un esempio di programmazione principale**

{{< highlight csharp >}}
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

## **Ottieni un master dal file Visio**
A volte, gli sviluppatori devono ottenere i dettagli del master di un disegno Visio. Il Aspose.Diagram API supporta questa funzione.

 Aspose.Diagram for .NET offre il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class che rappresenta un disegno Visio. La proprietà Masters, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Master. Questa proprietà può essere utilizzata per recuperare i dettagli di un particolare master. La classe MasterCollection espone i metodi GetMasterByName e GetMaster che possono essere chiamati per ottenere un oggetto Master.
### **Ottenere un oggetto master per ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiama il metodo GetMaster della classe Diagram.Masters.
#### **Oggetto principale per esempio di programmazione ID**
L'esempio seguente mostra come ottenere un master per ID da un disegno Visio.


{{< highlight csharp >}}
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

### **Ottenere un oggetto principale per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetMasterByName della classe Diagram.Masters.
#### **Esempio di programmazione oggetto master per nome**
L'esempio seguente mostra come ottenere un oggetto principale per nome da un disegno Visio.


{{< highlight csharp >}}
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

## **Verificare Presenza di un Maestro nel Disegno Visio**
Il Aspose.Diagram API supporta il controllo della presenza di un master in un disegno Visio. Con la proprietà MasterCollection, gli sviluppatori possono verificare se un master è presente in base al nome o all'ID.

 Aspose.Diagram for .NET offre il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio. La proprietà Masters, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Master. Questa proprietà può essere utilizzata per verificare la presenza di un particolare master. La classe MasterCollection espone il metodo IsExist che può essere chiamato con il nome master o il parametro ID.
### **Controllo di una presenza principale tramite ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo IsExist della classe Diagram.Masters.
#### **Presenza principale tramite esempio di programmazione ID**
L'esempio seguente mostra come verificare la presenza di un master per ID in un disegno Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Master();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Check master by id
bool isPresent = diagram.Masters.IsExist(2);

Console.WriteLine("Master Presence : " + isPresent);

{{< /highlight >}}

### **Controllo di una presenza principale per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo IsExist della classe Diagram.Masters.
#### **Esempio di programmazione della presenza principale per nome**
L'esempio seguente mostra come controllare una presenza master per nome dal disegno Visio.


{{< highlight csharp >}}
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

