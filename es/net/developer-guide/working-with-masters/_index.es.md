---
title: Trabajando con Maestros
type: docs
weight: 70
url: /es/net/working-with-masters/
description: Esta sección explica cómo agregar maestro u obtener información maestra con Aspose.Diagram.
---
## **Recuperación de información maestra**
Un patrón de forma es otro nombre para una plantilla Visio. Con Aspose.Diagram, es posible recuperar información sobre páginas, conectores y también maestros. Este artículo explica cómo obtener el ID y el nombre de un diagram.

 los[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objeto representa un[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maestro del objeto en un diagram. La propiedad Masters, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Master. Esta propiedad se puede utilizar para recuperar la información de los maestros, es decir, el ID y el nombre del maestro. Utilice la propiedad Page.Shapes para determinar qué forma ha heredado la forma maestra.
### **Muestra de programación de recuperación de información maestra**
El siguiente fragmento de código recupera la información maestra de un diagram.


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

## **Agregar maestro desde la plantilla de formas**
Una plantilla es una colección de formas asociadas con una plantilla Microsoft Office Visio particular. Con Aspose.Diagram, es posible agregar cualquier patrón de forma a un dibujo desde una plantilla.
### **Agregar maestro**
 los[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objeto representa un[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maestro del objeto en un diagram. El método AddMaster, expuesto por la clase Diagram, permite agregar un maestro desde una plantilla. Ofrece las siguientes cuatro formas:

- Ruta del archivo de plantilla e ID principal.
- Ruta del archivo de plantilla y nombre principal.
- Secuencia de archivo de plantilla e ID maestro.
- Flujo de archivo de plantilla y nombre maestro.
- Agregar maestro a diagram desde la fuente diagram
#### **Agregar muestra de programación maestra**

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

## **Crear maestro desde cero**
 Aspose.Diagram API permite crear un[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) desde cero sin ningún stencil, dibujo o plantilla. Los desarrolladores pueden personalizar la creación de Master. El método AddMaster, expuesto por la clase Diagram, permite agregar un maestro.
### **Crear muestra de programación maestra**

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

## **Obtenga un Máster del Archivo Visio**
A veces, los desarrolladores necesitan obtener los detalles del maestro de un dibujo Visio. El Aspose.Diagram API admite esta función.

 Aspose.Diagram for .NET ofrece la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)clase que representa un dibujo Visio. La propiedad Masters, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Master. Esta propiedad se puede utilizar para recuperar los detalles de un maestro en particular. La clase MasterCollection expone los métodos GetMasterByName y GetMaster a los que se puede llamar para obtener un objeto Master.
### **Obtener un objeto maestro por ID**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetMaster de la clase Diagram.Masters.
#### **Ejemplo de programación de objeto maestro por ID**
El siguiente ejemplo muestra cómo obtener un maestro por ID de un dibujo Visio.


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

### **Obtener un objeto maestro por nombre**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetMasterByName de la clase Diagram.Masters.
#### **Ejemplo de programación de objeto maestro por nombre**
El siguiente ejemplo muestra cómo obtener un objeto maestro por nombre de un dibujo Visio.


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

## **Compruebe la presencia de un maestro en el dibujo Visio**
El Aspose.Diagram API admite la comprobación de la presencia de un maestro en un dibujo Visio. Con la propiedad MasterCollection, los desarrolladores pueden verificar si un maestro está presente por su nombre o ID.

 Aspose.Diagram for .NET ofrece la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase que representa un dibujo Visio. La propiedad Masters, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Master. Esta propiedad se puede utilizar para comprobar la presencia de un maestro en particular. La clase MasterCollection expone el método IsExist al que se puede llamar con el nombre maestro o el parámetro ID.
### **Comprobación de una presencia maestra por ID**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método IsExist de la clase Diagram.Masters.
#### **Ejemplo de programación de Master Presence by ID**
El siguiente ejemplo muestra cómo verificar la presencia de un maestro por ID en un dibujo Visio.


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

### **Comprobación de la presencia de un maestro por nombre**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método IsExist de la clase Diagram.Masters.
#### **Ejemplo de programación de presencia maestra por nombre**
El siguiente ejemplo muestra cómo verificar la presencia de un maestro por nombre del dibujo Visio.


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

