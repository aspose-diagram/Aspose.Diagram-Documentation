---
title: Working with Masters
type: docs
weight: 70
url: /net/working-with-masters/
description: This section explains how to add master or get master information with Aspose.Diagram.
---

## **Retrieving Master Information**
A shape master is another name for a Visio stencil. With Aspose.Diagram, it is possible to retrieve information about pages, connectors and also masters. This article explains how to get the ID and name from a diagram.

The [Master](http://www.aspose.com/api/net/diagram/aspose.diagram/master) object represents a [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object's master in a diagram. The Masters property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Master objects. This property can be used to retrieve the masters’ information that is, the master ID and name. Use the Page.Shapes property to determine which shape has been inherited by the master shape.
### **Retrieving Master Information Programming Sample**
The following piece of code retrieves the masters information from a diagram.


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

## **Add Master from the Stencil of Shapes**
A stencil is a collection of shapes associated with a particular Microsoft Office Visio template. With Aspose.Diagram, it is possible to add any shape master to a drawing from a stencil.
### **Add Master**
The [Master](http://www.aspose.com/api/net/diagram/aspose.diagram/master) object represents a [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object's master in a diagram. The AddMaster method, exposed by the Diagram class, allows adding a master from a stencil. It offers the following four ways:

- Stencil file path and master ID.
- Stencil file path and master name.
- Stencil file stream and master ID.
- Stencil file stream and master name.
- Add master to diagram from source diagram
#### **Add Master Programming Sample**

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

## **Create Master from Scratch**
Aspose.Diagram API allows to create a [Master](http://www.aspose.com/api/net/diagram/aspose.diagram/master) from scratch without any stencil, drawing or template. Developers can customize the creation of Master. The AddMaster method, exposed by the Diagram class, allows to add a master.
### **Create Master Programming Sample**

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

## **Get a Master from the Visio File**
Sometimes, developers need to get the details of a Visio drawing's master. The Aspose.Diagram API supports this feature.

Aspose.Diagram for .NET offers the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The Masters property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Master objects. This property can be used to retrieve a particular master's details. The MasterCollection class exposes the GetMasterByName and GetMaster methods which can be called to get a Master object.
### **Getting a Master Object by ID**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' GetMaster method.
#### **Master Object by ID Programming Sample**
The following example shows how to get a master by ID from a Visio drawing.


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

### **Getting a Master Object by Name**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' GetMasterByName method.
#### **Master Object by Name Programming Sample**
The following example shows how to get a master object by name from a Visio drawing.


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

## **Check Presence of a Master in the Visio Drawing**
The Aspose.Diagram API supports checking for the presence of a master in a Visio drawing. With the MasterCollection property, developers can check to see if a master is present by its name or ID.

Aspose.Diagram for .NET offers the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The Masters property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Master objects. This property can be used to check for the presence of a particular master. The MasterCollection class exposes the IsExist method which can be called with the master name or ID parameter.
### **Checking a Master Presence by ID**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' IsExist method.
#### **Master Presence by ID Programming Sample**
The following example shows how to check presence of a master by ID in a Visio drawing.


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

### **Checking a Master Presence by Name**
This example work as follows:

1. Create an object of the Diagram class.
1. Call the Diagram.Masters class' IsExist method.
#### **Master Presence by Name Programming Sample**
The following example shows how to check a master presence by name from Visio drawing.


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

