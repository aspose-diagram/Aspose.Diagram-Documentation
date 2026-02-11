---
title: Travailler avec les maîtres
type: docs
weight: 70
url: /fr/net/working-with-masters/
description: Cette section explique comment ajouter un maître ou obtenir des informations sur le maître avec Aspose.Diagram.
---
## **Récupération des informations sur le maître**
Un maître de forme est un autre nom pour un gabarit Visio. Avec Aspose.Diagram, il est possible de récupérer des informations sur les pages, les connecteurs et aussi les masters. Cet article explique comment obtenir l'ID et le nom d'un diagram.

 La[Maître](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'objet représente un[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maître de l'objet dans un diagram. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour récupérer les informations des maîtres, c'est-à-dire l'ID et le nom du maître. Utilisez la propriété Page.Shapes pour déterminer quelle forme a été héritée par la forme de base.
### **Récupération de l'exemple de programmation des informations principales**
Le morceau de code suivant récupère les informations des maîtres à partir d'un diagram.


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

## **Ajouter un maître à partir du gabarit de formes**
Un gabarit est une collection de formes associées à un gabarit particulier. Avec Aspose.Diagram, il est possible d'ajouter n'importe quel maître de forme à un dessin à partir d'un pochoir.
### **Ajouter maître**
 La[Maître](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'objet représente un[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maître de l'objet dans un diagram. La méthode AddMaster, exposée par la classe Diagram, permet d'ajouter un maître à partir d'un gabarit. Il propose les quatre manières suivantes :

- Chemin d'accès au fichier Stencil et ID principal.
- Chemin d'accès au fichier Stencil et nom du masque.
- Flux de fichiers Stencil et ID maître.
- Flux de fichier Stencil et nom du maître.
- Ajouter le maître à diagram à partir de la source diagram
#### **Ajouter un exemple de programmation maître**

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

## **Créer un maître à partir de zéro**
 Aspose.Diagram API permet de créer un[Maître](http://www.aspose.com/api/net/diagram/aspose.diagram/master) à partir de zéro sans aucun pochoir, dessin ou modèle. Les développeurs peuvent personnaliser la création de Master. La méthode AddMaster, exposée par la classe Diagram, permet d'ajouter un maître.
### **Créer un exemple de programmation maître**

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

## **Obtenir un Master à partir du fichier Visio**
Parfois, les développeurs ont besoin d'obtenir les détails d'un maître de dessin Visio. Le Aspose.Diagram API prend en charge cette fonctionnalité.

 Aspose.Diagram for .NET offre le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)classe qui représente un dessin Visio. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour récupérer les détails d'un maître particulier. La classe MasterCollection expose les méthodes GetMasterByName et GetMaster qui peuvent être appelées pour obtenir un objet Master.
### **Obtenir un objet principal par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetMaster de la classe Diagram.Masters.
#### **Exemple de programmation d'objet maître par ID**
L'exemple suivant montre comment obtenir une forme de base par ID à partir d'un dessin Visio.


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

### **Obtenir un objet principal par nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetMasterByName de la classe Diagram.Masters.
#### **Exemple de programmation d'objet maître par nom**
L'exemple suivant montre comment obtenir un objet principal par son nom à partir d'un dessin Visio.


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

## **Vérifier la présence d'un maître dans le dessin Visio**
Le Aspose.Diagram API prend en charge la vérification de la présence d'un maître dans un dessin Visio. Avec la propriété MasterCollection, les développeurs peuvent vérifier si un maître est présent par son nom ou son ID.

 Aspose.Diagram for .NET offre le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe qui représente un dessin Visio. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour vérifier la présence d'un maître particulier. La classe MasterCollection expose la méthode IsExist qui peut être appelée avec le nom principal ou le paramètre ID.
### **Vérifier la présence d'un maître par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode IsExist de la classe Diagram.Masters.
#### **Présence principale par exemple de programmation ID**
L'exemple suivant montre comment vérifier la présence d'un maître par ID dans un dessin Visio.


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

### **Vérifier la présence d'un maître par son nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode IsExist de la classe Diagram.Masters.
#### **Exemple de programmation de présence principale par nom**
L'exemple suivant montre comment vérifier la présence d'un maître par son nom à partir du dessin Visio.


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

