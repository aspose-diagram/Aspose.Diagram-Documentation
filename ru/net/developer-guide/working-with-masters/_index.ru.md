---
title: Работа с мастерами
type: docs
weight: 70
url: /ru/net/working-with-masters/
description: В этом разделе объясняется, как добавить мастер или получить информацию о мастере с помощью Aspose.Diagram.
---
## **Получение основной информации**
Мастер формы — это другое название трафарета Visio. С помощью Aspose.Diagram можно получить информацию о страницах, соединителях и мастерах. В этой статье объясняется, как получить идентификатор и имя по номеру diagram.

[Мастер](http://www.aspose.com/api/net/diagram/aspose.diagram/master) объект представляет собой[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) мастер объекта в diagram. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения информации о мастере, т. е. идентификатора и имени мастера. Используйте свойство Page.Shapes, чтобы определить, какая фигура была унаследована эталонной фигурой.
### **Пример программирования получения основной информации**
Следующий фрагмент кода извлекает информацию об основных устройствах из файла diagram.


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

## **Добавить мастер из трафарета фигур**
Трафарет — это набор фигур, связанных с определенным шаблоном Microsoft Office Visio. С помощью Aspose.Diagram можно добавить любой образец формы к рисунку из трафарета.
### **Добавить мастера**
[Мастер](http://www.aspose.com/api/net/diagram/aspose.diagram/master) объект представляет собой[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) мастер объекта в diagram. Метод AddMaster, предоставляемый классом Diagram, позволяет добавлять мастер из трафарета. Он предлагает следующие четыре способа:

- Путь к файлу трафарета и мастер-идентификатор.
- Путь к файлу трафарета и имя мастера.
- Поток файла трафарета и мастер-идентификатор.
- Поток файла трафарета и мастер-имя.
- Добавить мастер в diagram из источника diagram
#### **Добавить образец основного программирования**

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

## **Создать мастер с нуля**
 Aspose.Diagram API позволяет создать[Мастер](http://www.aspose.com/api/net/diagram/aspose.diagram/master) с нуля без всяких трафаретов, рисунков и шаблонов. Разработчики могут настроить создание Мастера. Метод AddMaster, предоставляемый классом Diagram, позволяет добавить мастер.
### **Создать основной образец программирования**

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

## **Получить мастер из файла Visio**
Иногда разработчикам необходимо получить подробную информацию о мастере чертежа Visio. Aspose.Diagram API поддерживает эту функцию.

 Aspose.Diagram for .NET предлагает[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения сведений об определенном мастере. Класс MasterCollection предоставляет методы GetMasterByName и GetMaster, которые можно вызывать для получения объекта Master.
### **Получение Мастер-объекта по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMaster класса Diagram.Masters.
#### **Образец программирования главного объекта по идентификатору**
В следующем примере показано, как получить мастер по идентификатору из чертежа Visio.


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

### **Получение главного объекта по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMasterByName класса Diagram.Masters.
#### **Образец программирования основного объекта по имени**
В следующем примере показано, как получить мастер-объект по имени из чертежа Visio.


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

## **Проверить наличие мастера в чертеже Visio**
Aspose.Diagram API поддерживает проверку наличия мастера в чертеже Visio. С помощью свойства MasterCollection разработчики могут проверить наличие мастера по его имени или идентификатору.

 Aspose.Diagram for .NET предлагает[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для проверки наличия определенного мастера. Класс MasterCollection предоставляет метод IsExist, который можно вызывать с помощью имени мастера или параметра ID.
### **Проверка присутствия Мастера по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by ID**
В следующем примере показано, как проверить наличие мастера по идентификатору в чертеже Visio.


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

### **Проверка присутствия мастера по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by Name**
В следующем примере показано, как проверить наличие мастера по имени из чертежа Visio.


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

