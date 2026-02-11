---
title: 与大师合作
type: docs
weight: 70
url: /zh/net/working-with-masters/
description: 本节介绍如何使用 Aspose.Diagram 添加 master 或获取 master 信息。
---
## **检索主信息**
形状母版是 Visio 模板的另一个名称。使用 Aspose.Diagram，可以检索有关页面、连接器和母版的信息。本文介绍如何从 diagram 获取 ID 和名称。

这[掌握](http://www.aspose.com/api/net/diagram/aspose.diagram/master)对象代表一个[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)对象在 diagram 中的主人。由 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检索主人的信息，即主人 ID 和名称。使用 Page.Shapes 属性确定主控形状继承了哪个形状。
### **检索主信息编程示例**
以下代码段从 diagram 中检索主人信息。

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
## **从形状模板添加母版**
模板是与特定 Microsoft Office Visio 模板相关联的形状集合。使用 Aspose.Diagram，可以将任何形状母版添加到模板中的绘图中。
### **添加大师**
这[掌握](http://www.aspose.com/api/net/diagram/aspose.diagram/master)对象代表一个[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)对象在 diagram 中的母版。由 Diagram 类公开的 AddMaster 方法允许从模板添加母版。它提供了以下四种方式：

- 模板文件路径和主 ID。
- 模板文件路径和主名称。
- 模板文件流和主 ID。
- 模板文件流和主名称。
- 从源 diagram 添加 master 到 diagram
#### **添加主程序示例**
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
## **从头开始创建大师**
 Aspose.Diagram API 允许创建一个[掌握](http://www.aspose.com/api/net/diagram/aspose.diagram/master)从头开始，没有任何模板、绘图或模板。开发者可以自定义创建Master。 Diagram 类公开的 AddMaster 方法允许添加主控。
### **创建主程序示例**
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
## **从Visio文件中获取大师**
有时，开发人员需要获得 Visio 图纸的主人的详细信息。 Aspose.Diagram API 支持此功能。

 Aspose.Diagram for .NET 提供[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检索特定主人的详细信息。 MasterCollection 类公开了 GetMasterByName 和 GetMaster 方法，可以调用这些方法来获取 Master 对象。
### **通过 ID 获取主对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 GetMaster 方法。
#### **按 ID 编程示例的主对象**
以下示例显示如何通过 ID 从 Visio 绘图中获取母版。

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
### **按名称获取主对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 GetMasterByName 方法。
#### **按名称编程示例的主对象**
以下示例显示如何从 Visio 绘图中按名称获取主对象。

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
## **检查 Visio 绘图中是否存在大师**
Aspose.Diagram API 支持检查 Visio 绘图中是否存在母版。使用 MasterCollection 属性，开发人员可以通过名称或 ID 检查母版是否存在。

 Aspose.Diagram for .NET 提供[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检查特定主机的存在。 MasterCollection 类公开了可以使用主名称或 ID 参数调用的 IsExist 方法。
### **通过 ID 检查主状态**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 IsExist 方法。
#### **Master Presence by ID 编程示例**
以下示例显示如何在 Visio 图形中按 ID 检查主控图是否存在。

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
### **按名称检查主状态**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 IsExist 方法。
#### **Master Presence by Name 编程示例**
以下示例显示如何按名称检查 Visio 图形中的主控存在。

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
