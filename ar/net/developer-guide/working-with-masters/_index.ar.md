---
title: العمل مع الماجستير
type: docs
weight: 70
url: /ar/net/working-with-masters/
description: يشرح هذا القسم كيفية إضافة معلومات رئيسية أو الحصول على معلومات رئيسية باستخدام Aspose.Diagram.
---
## **استرجاع معلومات الماجستير**
سيد الشكل هو اسم آخر لاستنسل Visio. باستخدام Aspose.Diagram ، يمكن استرجاع معلومات حول الصفحات والموصلات وأيضًا الرئيسية. تشرح هذه المقالة كيفية الحصول على المعرف والاسم من diagram.

 ال[يتقن](http://www.aspose.com/api/net/diagram/aspose.diagram/master) الكائن يمثل أ[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) كائن رئيسي في diagram. الخاصية الرئيسية ، التي تم الكشف عنها بواسطة الفئة Diagram ، تدعم مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية لاسترداد المعلومات الرئيسية وهي المعرف الرئيسي والاسم. استخدم خاصية Page.Shapes لتحديد الشكل الذي ورثه الشكل الرئيسي.
### **استرجاع نموذج برمجة معلومات الماجستير**
يسترد جزء الكود التالي المعلومات الرئيسية من diagram.


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

## **أضف ماستر من استنسل الأشكال**
الاستنسل هو مجموعة من الأشكال المرتبطة بقالب Microsoft Office Visio معين. باستخدام Aspose.Diagram ، يمكن إضافة أي شكل رئيسي إلى رسم من استنسل.
### **إضافة ماجستير**
 ال[يتقن](http://www.aspose.com/api/net/diagram/aspose.diagram/master) الكائن يمثل أ[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) كائن رئيسي في diagram. تسمح طريقة AddMaster ، المكشوفة بواسطة فئة Diagram ، بإضافة رئيسي من استنسل. يقدم الطرق الأربع التالية:

- مسار ملف الاستنسل والمعرف الرئيسي.
- مسار ملف الاستنسل والاسم الرئيسي.
- دفق ملف الاستنسل والمعرف الرئيسي.
- دفق ملف الاستنسل والاسم الرئيسي.
- أضف رئيسي إلى diagram من المصدر diagram
#### **إضافة عينة البرمجة الرئيسية**

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

## **إنشاء ماجستير من الصفر**
 Aspose.Diagram API يسمح بإنشاء ملف[يتقن](http://www.aspose.com/api/net/diagram/aspose.diagram/master) من الصفر دون أي استنسل أو رسم أو قالب. يمكن للمطورين تخصيص إنشاء Master. تسمح طريقة AddMaster ، التي تم الكشف عنها بواسطة فئة Diagram ، بإضافة عنصر رئيسي.
### **إنشاء عينة البرمجة الرئيسية**

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

## **احصل على درجة الماجستير من ملف Visio**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل سيد رسم Visio. يدعم Aspose.Diagram API هذه الميزة.

 يقدم Aspose.Diagram for .NET[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)فئة تمثل رسم Visio. تدعم الخاصية Masters ، المكشوفة بواسطة الفئة Diagram ، مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية لاسترداد تفاصيل رئيسية معينة. تعرض فئة MasterCollection أساليب GetMasterByName و GetMaster التي يمكن استدعاؤها للحصول على كائن رئيسي.
### **الحصول على كائن رئيسي بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل بـ Diagram.Masters class 'GetMaster method.
#### **كائن رئيسي عن طريق نموذج برمجة معرف**
يوضح المثال التالي كيفية الحصول على سيد بواسطة المعرف من رسم Visio.


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

### **الحصول على كائن رئيسي بالاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Masters class 'أسلوب GetMasterByName.
#### **كائن رئيسي حسب عينة برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن رئيسي بالاسم من رسم Visio.


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

## **تحقق من وجود ماجستير في رسم Visio**
يدعم Aspose.Diagram API التحقق من وجود سيد في رسم Visio. باستخدام خاصية MasterCollection ، يمكن للمطورين التحقق لمعرفة ما إذا كان المعلم موجودًا بالاسم أو المعرف.

 يقدم Aspose.Diagram for .NET[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم الخاصية Masters ، المكشوفة بواسطة الفئة Diagram ، مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية للتحقق من وجود سيد معين. تعرض فئة MasterCollection طريقة IsExist التي يمكن استدعاؤها بالاسم الرئيسي أو معلمة المعرف.
### **التحقق من وجود رئيسي عن طريق المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Masters class 'طريقة IsExist.
#### **حضور ماجستير عن طريق نموذج برمجة معرف**
يوضح المثال التالي كيفية التحقق من وجود رئيسي بواسطة المعرف في رسم Visio.


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

### **التحقق من وجود رئيسي بالاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Masters class 'طريقة IsExist.
#### **حضور ماجستير من خلال نموذج برمجة الاسم**
يوضح المثال التالي كيفية التحقق من وجود رئيسي بالاسم من رسم Visio.


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

