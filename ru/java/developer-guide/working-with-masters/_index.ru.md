---
title: Работа с мастерами
type: docs
weight: 30
url: /ru/java/working-with-masters/
---
## **Получение основной информации**
Мастер формы — это другое название трафарета Visio. С помощью Aspose.Diagram можно получить информацию о страницах, соединителях, а также мастерах. В этой статье объясняется, как получить идентификатор и имя по номеру diagram.

[Мастер](https://reference.aspose.com/diagram/java/com.aspose.diagram/master) объект представляет собой[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)мастер объекта в diagram. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения информации о мастере, т. е. идентификатора и имени мастера.

Используйте свойство Page.Shapes, чтобы определить, какая фигура была унаследована эталонной фигурой.

**Окно консоли, показывающее вывод кода.** 

![дело:изображение_альтернативный_текст](http://i.imgur.com/DPn5sP9.png)
### **Пример программирования получения основной информации**
Следующий фрагмент кода извлекает информацию об основных устройствах из файла diagram.


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

## **Добавить мастер из трафарета фигур**
Трафарет — это набор фигур, связанных с определенным шаблоном Microsoft Office Visio. С помощью Aspose.Diagram можно добавить любой образец формы к рисунку из трафарета.
### **Добавить мастера**
Объект Master представляет мастер объекта Shape в diagram. Метод AddMaster, предоставляемый классом Diagram, позволяет добавлять мастер из трафарета. Он предлагает следующие четыре способа:

- Путь к файлу трафарета и мастер-идентификатор.
- Путь к файлу трафарета и имя мастера.
- Поток файла трафарета и мастер-идентификатор.
- Поток файла трафарета и мастер-имя.
- Добавить мастер в diagram из источника diagram
#### **Добавить образец основного программирования**

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

## **Создать мастер с нуля**
Aspose.Diagram API позволяет создать мастер с нуля без использования трафарета, рисунка или шаблона. Разработчики могут настроить создание Мастера. Метод addMaster, предоставляемый классом Diagram, позволяет добавить мастер.
#### **Создать основной образец программирования**

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

## **Получить мастер из файла Visio**
Иногда разработчикам необходимо получить подробную информацию о мастере чертежа Visio. Aspose.Diagram API поддерживает эту функцию.

 Aspose.Diagram for Java предлагает[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения сведений об определенном мастере. Класс MasterCollection предоставляет методы GetMasterByName и GetMaster, которые можно вызывать для получения объекта Master.
### **Получение Мастер-объекта по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMaster класса Diagram.Masters.
#### **Образец программирования главного объекта по идентификатору**
В следующем примере показано, как получить мастер по идентификатору из чертежа Visio.


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

### **Получение главного объекта по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMasterByName класса Diagram.Masters.
#### **Образец программирования основного объекта по имени**
В следующем примере показано, как получить мастер-объект по имени из чертежа Visio.


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

## **Проверить наличие мастера в чертеже Visio**
Aspose.Diagram API поддерживает проверку наличия мастера в чертеже Visio. С помощью свойства MasterCollection разработчики могут проверить наличие мастера по его имени или идентификатору.

 Aspose.Diagram for Java предлагает[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для проверки наличия определенного мастера. Класс MasterCollection предоставляет метод IsExist, который можно вызывать с помощью имени мастера или параметра ID.
### **Проверка присутствия Мастера по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by ID**
В следующем примере показано, как проверить наличие мастера по идентификатору в чертеже Visio.


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

### **Проверка присутствия мастера по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by Name**
В следующем примере показано, как проверить наличие мастера по имени из чертежа Visio.


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

