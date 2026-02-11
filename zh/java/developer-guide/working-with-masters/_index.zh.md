---
title: 与大师合作
type: docs
weight: 30
url: /zh/java/working-with-masters/
---
## **检索主信息**
形状母版是 Visio 模板的另一个名称。使用 Aspose.Diagram，可以检索有关页面、连接器和母版的信息。本文介绍如何从 diagram 获取 ID 和名称。

这[掌握](https://reference.aspose.com/diagram/java/com.aspose.diagram/master)对象代表一个[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)对象在 diagram 中的主人。由 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检索主人的信息，即主人 ID 和名称。

使用 Page.Shapes 属性确定主控形状继承了哪个形状。

**显示代码输出的控制台窗口。** 

![待办事项：图片_替代_文本](http://i.imgur.com/DPn5sP9.png)
### **检索主信息编程示例**
以下代码段从 diagram 中检索主人信息。


{{< highlight java >}}
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

## **从形状模板添加母版**
模板是与特定 Microsoft Office Visio 模板相关联的形状集合。使用 Aspose.Diagram，可以将任何形状母版添加到模板中的绘图中。
### **添加大师**
Master 对象表示 diagram 中 Shape 对象的母版。Diagram 类公开的 AddMaster 方法允许从模板添加母版。它提供了以下四种方式：

- 模板文件路径和主 ID。
- 模板文件路径和主名称。
- 模板文件流和主 ID。
- 模板文件流和主名称。
- 从源 diagram 添加 master 到 diagram
#### **添加主程序示例**

{{< highlight java >}}
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

## **从头开始创建大师**
Aspose.Diagram API 允许在没有任何模板、绘图或模板的情况下从头开始创建母版。开发者可以自定义创建Master。 Diagram 类公开的 addMaster 方法允许添加主控。
#### **创建主程序示例**

{{< highlight java >}}
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



{{< highlight java >}}
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

## **从Visio文件中获取大师**
有时，开发人员需要获得 Visio 图纸的主人的详细信息。 Aspose.Diagram API 支持此功能。

 Aspose.Diagram for Java 提供[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检索特定主人的详细信息。 MasterCollection 类公开了 GetMasterByName 和 GetMaster 方法，可以调用这些方法来获取 Master 对象。
### **通过 ID 获取主对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 GetMaster 方法。
#### **按 ID 编程示例的主对象**
以下示例显示如何通过 ID 从 Visio 绘图中获取母版。


{{< highlight java >}}
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

### **按名称获取主对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 GetMasterByName 方法。
#### **按名称编程示例的主对象**
以下示例显示如何从 Visio 绘图中按名称获取主对象。


{{< highlight java >}}
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

## **检查 Visio 绘图中是否存在大师**
Aspose.Diagram API 支持检查 Visio 绘图中是否存在母版。使用 MasterCollection 属性，开发人员可以通过名称或 ID 检查母版是否存在。

 Aspose.Diagram for Java 提供[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检查特定主机的存在。 MasterCollection 类公开了可以使用主名称或 ID 参数调用的 IsExist 方法。
### **通过 ID 检查主状态**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 IsExist 方法。
#### **Master Presence by ID 编程示例**
以下示例显示如何在 Visio 图形中按 ID 检查主控图是否存在。


{{< highlight java >}}
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

### **按名称检查主状态**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 IsExist 方法。
#### **Master Presence by Name 编程示例**
以下示例显示如何按名称检查 Visio 图形中的主控存在。


{{< highlight java >}}
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

