---
title: Ustalarla Çalışmak
type: docs
weight: 70
url: /tr/net/working-with-masters/
description: Bu bölümde Aspose.Diagram ile master ekleme veya master bilgilerinin nasıl alınacağı açıklanmaktadır.
---
## **Ana Bilgileri Alma**
Bir şekil ustası, Visio şablonunun başka bir adıdır. Aspose.Diagram ile sayfalar, konektörler ve ayrıca master'lar hakkında bilgi almak mümkündür. Bu makalede, bir diagram numaralı telefondan kimliğin ve adın nasıl alınacağı açıklanmaktadır.

 bu[Usta](http://www.aspose.com/api/net/diagram/aspose.diagram/master) nesne temsil eder[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) diagram'de nesnenin yöneticisi. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesnelerinin bir koleksiyonunu destekler. Bu özellik, ana kimliği ve adı olan ana bilgileri almak için kullanılabilir. Ana şekil tarafından hangi şeklin devralındığını belirlemek için Page.Shapes özelliğini kullanın.
### **Ana Bilgi Programlama Örneğinin Alınması**
Aşağıdaki kod parçası, bir diagram'den ana bilgileri alır.


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

## **Şekiller Şablonundan Master Ekleme**
Şablon, belirli bir Microsoft Office Visio şablonuyla ilişkili bir şekil koleksiyonudur. Aspose.Diagram ile bir şablondan bir çizime herhangi bir ana şekil eklemek mümkündür.
### **Usta Ekle**
 bu[Usta](http://www.aspose.com/api/net/diagram/aspose.diagram/master) nesne temsil eder[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) diagram'de nesnenin yöneticisi. Diagram sınıfı tarafından sunulan AddMaster yöntemi, bir şablondan bir ana öğe eklenmesine izin verir. Aşağıdaki dört yolu sunar:

- Şablon dosyası yolu ve ana kimlik.
- Şablon dosyası yolu ve ana adı.
- Şablon dosyası akışı ve ana kimlik.
- Şablon dosyası akışı ve ana ad.
- diagram kaynağından diagram'e master ekleyin
#### **Ana Programlama Örneği Ekle**

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

## **Sıfırdan Usta Oluştur**
 Aspose.Diagram API oluşturmaya izin verir[Usta](http://www.aspose.com/api/net/diagram/aspose.diagram/master) herhangi bir şablon, çizim veya şablon olmadan sıfırdan. Geliştiriciler, Master'ın oluşturulmasını özelleştirebilir. Diagram sınıfı tarafından sunulan AddMaster yöntemi, bir ana öğe eklenmesine izin verir.
### **Ana Programlama Örneği Oluşturma**

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

## **Visio Dosyasından Master Alın**
Bazen, geliştiricilerin bir Visio çizim ustasının ayrıntılarını alması gerekir. Aspose.Diagram API bu özelliği destekler.

 Aspose.Diagram for .NET sunuyor[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesne koleksiyonunu destekler. Bu özellik, belirli bir master'ın ayrıntılarını almak için kullanılabilir. MasterCollection sınıfı, bir Master nesnesi almak için çağrılabilen GetMasterByName ve GetMaster yöntemlerini kullanıma sunar.
### **Kimliğe göre Ana Nesne Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının GetMaster yöntemini çağırın.
#### **Kimliğe Göre Ana Nesne Programlama Örneği**
Aşağıdaki örnek, bir Visio çiziminden kimliğe göre nasıl master alınacağını gösterir.


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

### **Ada Göre Ana Nesne Alma**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının GetMasterByName yöntemini çağırın.
#### **İsme Göre Ana Nesne Programlama Örneği**
Aşağıdaki örnek, bir Visio çiziminden ada göre bir ana nesnenin nasıl alınacağını gösterir.


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

## **Visio Çiziminde Master Varlığını Kontrol Edin**
Aspose.Diagram API, Visio çiziminde bir master olup olmadığını kontrol etmeyi destekler. MasterCollection özelliği ile geliştiriciler, adına veya kimliğine göre bir master olup olmadığını kontrol edebilir.

 Aspose.Diagram for .NET sunuyor[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Visio çizimini temsil eden sınıf. Diagram sınıfı tarafından sunulan Masters özelliği, Aspose.Diagram.Master nesne koleksiyonunu destekler. Bu özellik, belirli bir ana öğenin varlığını kontrol etmek için kullanılabilir. MasterCollection sınıfı, master adı veya ID parametresi ile çağrılabilen IsExist yöntemini gösterir.
### **Kimliğe göre Ana Varlığı kontrol etme**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının IsExist yöntemini çağırın.
#### **ID Programlama Örneği ile Master Presence**
Aşağıdaki örnek, bir Visio çiziminde kimliğe göre bir master varlığının nasıl kontrol edileceğini gösterir.


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

### **Ada Göre Ana Varlığı Kontrol Etme**
Bu örnek şu şekilde çalışır:

1. Diagram sınıfından bir nesne oluşturun.
1. Diagram.Masters sınıfının IsExist yöntemini çağırın.
#### **Ada Göre Master Presence Programlama Örneği**
Aşağıdaki örnek, Visio çiziminden ada göre bir master varlığının nasıl kontrol edileceğini gösterir.


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

