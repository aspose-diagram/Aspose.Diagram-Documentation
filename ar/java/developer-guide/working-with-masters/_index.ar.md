---
title: العمل مع الماجستير
type: docs
weight: 30
url: /ar/java/working-with-masters/
---
## **استرجاع معلومات الماجستير**
سيد الشكل هو اسم آخر لاستنسل Visio. باستخدام Aspose.Diagram ، يمكن استرجاع معلومات حول الصفحات والموصلات وأيضًا الرئيسية. تشرح هذه المقالة كيفية الحصول على المعرف والاسم من diagram.

 ال[يتقن](https://reference.aspose.com/diagram/java/com.aspose.diagram/master) الكائن يمثل أ[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)كائن رئيسي في diagram. الخاصية الرئيسية ، التي تم الكشف عنها بواسطة الفئة Diagram ، تدعم مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية لاسترداد المعلومات الرئيسية وهي المعرف الرئيسي والاسم.

استخدم خاصية Page.Shapes لتحديد الشكل الذي ورثه الشكل الرئيسي.

**نافذة وحدة التحكم تظهر الإخراج من الكود.** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/DPn5sP9.png)
### **استرجاع نموذج برمجة معلومات الماجستير**
يسترد جزء الكود التالي المعلومات الرئيسية من diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveMasterInfo.class);

//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "drawing.vdx");

for (Master master : (Iterable<Master>) diagram.getMasters())
{
    //Display information about the masters
    System.out.println("\nMaster ID : " + master.getID());
    System.out.println("Master Name : " + master.getName());
}

{{< /highlight >}}
```
## **أضف ماستر من استنسل الأشكال**
الاستنسل هو مجموعة من الأشكال المرتبطة بقالب Microsoft Office Visio معين. باستخدام Aspose.Diagram ، يمكن إضافة أي شكل رئيسي إلى رسم من استنسل.
### **إضافة ماجستير**
يمثل الكائن الرئيسي رئيسي كائن الشكل في diagram. تسمح طريقة AddMaster ، المكشوفة بواسطة فئة Diagram ، بإضافة رئيسي من استنسل. يقدم الطرق الأربع التالية:

- مسار ملف الاستنسل والمعرف الرئيسي.
- مسار ملف الاستنسل والاسم الرئيسي.
- دفق ملف الاستنسل والمعرف الرئيسي.
- دفق ملف الاستنسل والاسم الرئيسي.
- أضف رئيسي إلى diagram من المصدر diagram
#### **إضافة عينة البرمجة الرئيسية**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddMasterFromStencil.class);    
// Load diagram
Diagram diagram = new Diagram();

// Load stencil to a stream
String templateFileName = dataDir + "NetApp-FAS-series.vss";

// Add master with stencil file path and master id
String masterName = "FAS80xx rear empty";
diagram.addMaster(templateFileName, 2);

// Add master with stencil file path and master name
diagram.addMaster(templateFileName, masterName);

// adds master to diagram from source diagram
Diagram src = new Diagram(templateFileName);
diagram.addMaster(src, masterName);

// Adds shape with defined PinX and PinY.
diagram.addShape(2.0, 2.0, masterName, 0);
diagram.addShape(6.0, 6.0, masterName, 0);

// Adds shape with defined PinX,PinY,Width and Height.
diagram.addShape(7.0, 3.0, 1.5, 1.5, masterName, 0);

{{< /highlight >}}
```
## **إنشاء ماجستير من الصفر**
Aspose.Diagram API يسمح بإنشاء Master من البداية دون أي استنسل أو رسم أو قالب. يمكن للمطورين تخصيص إنشاء Master. تسمح طريقة addMaster ، التي تم الكشف عنها بواسطة فئة Diagram ، بإضافة عنصر رئيسي.
#### **إنشاء عينة البرمجة الرئيسية**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(CreateMasterfromScratch.class) + "Masters/";

// create a new template
Diagram diagram = new Diagram();
// add master
diagram.getMasters().add(createMaster(101, "Regular", dataDir + "icon.png"));
// save template
diagram.save(dataDir + "template_Out.vssx", SaveFileFormat.VSSX);


// create master	
public static Master createMaster(final int masterId, final String name, String file) throws Exception
{
	// set master properties
	Master ms = new Master();
	ms.setID(masterId);
	ms.setName(name);
	ms.setIconSize(1);
	ms.setAlignName(2);
	ms.setMatchByName(0);
	ms.setIconUpdate(BOOL.TRUE);
	ms.setPatternFlags(0);
	ms.setHidden(0);
	
	// set master's shape properties
	final Shape shape = new Shape();
	ms.getShapes().add(shape);
	
	final double width = 0.5443889263424177;
	final double height = 0.432916947568133;
	
	shape.setID(5);
	shape.setType(TypeValue.FOREIGN);
	
	shape.getXForm().getPinX().setValue(0.2221944631712089);
	shape.getXForm().getPinY().setValue(0.1666458473784065);
	shape.getXForm().getWidth().setValue(width);
	shape.getXForm().getHeight().setValue(height);
	shape.getXForm().getLocPinX().getUfe().setF("Width*0.5");
	shape.getXForm().getLocPinY().getUfe().setF("Height*0.5");
	shape.getXForm().getResizeMode().setValue(0);
	
	shape.getTextXForm().getTxtPinY().getUfe().setF("-TxtHeight/2");
	shape.getTextXForm().getTxtWidth().getUfe().setF("TEXTWIDTH(TheText)");
	shape.getTextXForm().getTxtHeight().getUfe().setF("TEXTHEIGHT(TheText, TxtWidth)");
	
	shape.getForeign().getImgOffsetX().setValue(0);
	shape.getForeign().getImgOffsetY().setValue(0);
	shape.getForeign().getImgWidth().setValue(width);
	shape.getForeign().getImgHeight().setValue(height);
	
	// set connection properties
	final Connection connection = new Connection();
	shape.getConnections().add(connection);
	
	connection.setID(1);
	connection.setNameU("All");
	connection.getX().setValue(0.22);
	connection.getX().getUfe().setF("Width*0.5");
	connection.getY().setValue(0.16);
	connection.getY().getUfe().setF("Height*0.5");
	connection.getDirX().setValue(0);
	connection.getDirY().setValue(0);
	connection.getType().setValue(0);
	connection.getAutoGen().setValue(BOOL.FALSE);
	connection.getPrompt().getUfe().setF("No Formula");
	
	shape.getForeignData().setForeignType(ForeignType.BITMAP);
	shape.getForeignData().setCompressionType(CompressionType.PNG);
	File f = new File(file);
	byte[] fileBytes = new byte[(int) f.length()];
	FileInputStream fis = new FileInputStream(f);
	fis.read(fileBytes);
	fis.close();
		    
	shape.getForeignData().setValue(fileBytes);
	
	return ms;
}


{{< /highlight >}}
```

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
private final static char map[] = { // 0 1 2 3 4 5 6 7
		'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', // 0
		'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', // 1
		'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', // 2
		'Y', 'Z', 'a', 'b', 'c', 'd', 'e', 'f', // 3
		'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', // 4
		'o', 'p', 'q', 'r', 's', 't', 'u', 'v', // 5
		'w', 'x', 'y', 'z', '0', '1', '2', '3', // 6
		'4', '5', '6', '7', '8', '9', '+', '/' // 7
};

private final String lineSeparator;
private final boolean splitLines;

public BASE64Encoder() {
	lineSeparator = System.getProperty("line.separator");
	splitLines = true;
}

final void encodeBuffer(final InputStream inStream, final Writer outStream) throws IOException {
	final byte[] tmpbuffer = new byte[57];
	while (true) {
		final int numBytes = readFully(inStream, tmpbuffer);
		if (numBytes == -1) {
			break;
		}
		for (int j = 0; j < numBytes; j += 3) {
			if ((j + 3) <= numBytes) {
				encodeAtom(outStream, tmpbuffer, j, 3);
			} else {
				encodeAtom(outStream, tmpbuffer, j, (numBytes) - j);
			}
		}
		if (splitLines) {
			outStream.write(lineSeparator);
		}
		if (numBytes < 57) {
			break;
		}
	}
}

public final String encodeBuffer(final byte[] aBuffer) {
	final StringWriter outStream = new StringWriter();// aBuffer.length +
														// aBuffer.length>>1);
	try {
		encodeBuffer(new ByteArrayInputStream(aBuffer), outStream);
	} catch (final IOException e) {
		e.printStackTrace();
	}
	return outStream.toString();
}

final void encodeAtom(final Writer outStream, final byte[] data, final int offset, final int len) throws IOException {
	final byte a;
	final byte b;
	final byte c;

	if (len == 1) {
		a = data[offset];
		b = 0;
		c = 0;
		outStream.write(map[(a >>> 2) & 0x3F]);
		outStream.write(map[((a << 4) & 0x30) + ((b >>> 4) & 0xf)]);
		outStream.write('=');
		outStream.write('=');
	} else if (len == 2) {
		a = data[offset];
		b = data[offset + 1];
		c = 0;
		outStream.write(map[(a >>> 2) & 0x3F]);
		outStream.write(map[((a << 4) & 0x30) + ((b >>> 4) & 0xf)]);
		outStream.write(map[((b << 2) & 0x3c) + ((c >>> 6) & 0x3)]);
		outStream.write('=');
	} else {
		a = data[offset];
		b = data[offset + 1];
		c = data[offset + 2];
		outStream.write(map[(a >>> 2) & 0x3F]);
		outStream.write(map[((a << 4) & 0x30) + ((b >>> 4) & 0xf)]);
		outStream.write(map[((b << 2) & 0x3c) + ((c >>> 6) & 0x3)]);
		outStream.write(map[c & 0x3F]);
	}
}

private final int readFully(final InputStream in, final byte[] buffer) throws IOException {
	final int len = buffer.length;
	for (int i = 0; i < len; i++) {
		final int q = in.read();
		if (q == -1) {
			return i;
		}
		buffer[i] = (byte) q;
	}
	return len;
}

{{< /highlight >}}
```
## **احصل على درجة الماجستير من ملف Visio**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل سيد رسم Visio. يدعم Aspose.Diagram API هذه الميزة.

 يقدم Aspose.Diagram for Java[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)فئة تمثل رسم Visio. تدعم الخاصية Masters ، المكشوفة بواسطة الفئة Diagram ، مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية لاسترداد تفاصيل رئيسية معينة. تعرض فئة MasterCollection أساليب GetMasterByName و GetMaster التي يمكن استدعاؤها للحصول على كائن رئيسي.
### **الحصول على كائن رئيسي بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل بـ Diagram.Masters class 'GetMaster method.
#### **كائن رئيسي عن طريق نموذج برمجة معرف**
يوضح المثال التالي كيفية الحصول على سيد بواسطة المعرف من رسم Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetMasterbyID.class);  
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "RetrieveMasterInfo.vdx");

// Set master id
int masterid = 2;
// Get master object by id
Master master = diagram.getMasters().getMaster(masterid);

System.out.println("Master ID : " + master.getID());
System.out.println("Master Name : " + master.getName());
System.out.println("Master Name : " + master.getUniqueID());

{{< /highlight >}}
```
### **الحصول على كائن رئيسي بالاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Masters class 'أسلوب GetMasterByName.
#### **كائن رئيسي حسب عينة برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن رئيسي بالاسم من رسم Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetMasterbyName.class);      
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Set master name
String masterName = "Circle";
// Get master object by name
Master master = diagram.getMasters().getMasterByName(masterName);

System.out.println("Master ID : " + master.getID());
System.out.println("Master Name : " + master.getName());
System.out.println("Master Name : " + master.getUniqueID());

{{< /highlight >}}
```
## **تحقق من وجود ماجستير في رسم Visio**
يدعم Aspose.Diagram API التحقق من وجود سيد في رسم Visio. باستخدام خاصية MasterCollection ، يمكن للمطورين التحقق لمعرفة ما إذا كان المعلم موجودًا بالاسم أو المعرف.

 يقدم Aspose.Diagram for Java[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تمثل رسم Visio. تدعم الخاصية Masters ، المكشوفة بواسطة الفئة Diagram ، مجموعة من Aspose.Diagram.Master الكائنات. يمكن استخدام هذه الخاصية للتحقق من وجود سيد معين. تعرض فئة MasterCollection طريقة IsExist التي يمكن استدعاؤها بالاسم الرئيسي أو معلمة المعرف.
### **التحقق من وجود رئيسي عن طريق المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Masters class 'طريقة IsExist.
#### **حضور ماجستير عن طريق نموذج برمجة معرف**
يوضح المثال التالي كيفية التحقق من وجود رئيسي بواسطة المعرف في رسم Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckMasterPresencebyID.class);    
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// set master id
int masterid = 2;
// check master by id
boolean isPresent = diagram.getMasters().isExist(2);

System.out.println("Master Presence : " + isPresent);

{{< /highlight >}}
```
### **التحقق من وجود رئيسي بالاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Masters class 'طريقة IsExist.
#### **حضور ماجستير من خلال نموذج برمجة الاسم**
يوضح المثال التالي كيفية التحقق من وجود رئيسي بالاسم من رسم Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckMasterPresencebyName.class);  
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Set master name
String masterName = "VNXe3100 Storage Processor Rear";
// check master object by name
boolean isPresent = diagram.getMasters().isExist(masterName);

System.out.println("Master Presence : " + isPresent);

{{< /highlight >}}
```
