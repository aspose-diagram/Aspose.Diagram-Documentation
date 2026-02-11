---
title: Arbeiten mit Meistern
type: docs
weight: 30
url: /de/java/working-with-masters/
---
## **Stammdaten abrufen**
Ein Shape-Master ist ein anderer Name für eine Visio-Schablone. Mit Aspose.Diagram können Informationen über Seiten, Konnektoren und auch Master abgerufen werden. Dieser Artikel erklärt, wie Sie die ID und den Namen von einer diagram erhalten.

 Das[Meister](https://reference.aspose.com/diagram/java/com.aspose.diagram/master) Objekt repräsentiert a[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)Master-Objekt in einem diagram. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um die Informationen des Masters abzurufen, d. h. die Master-ID und den Namen.

Verwenden Sie die Page.Shapes-Eigenschaft, um zu bestimmen, welche Form von der Masterform geerbt wurde.

**Ein Konsolenfenster, das die Ausgabe des Codes anzeigt.** 

![todo: Bild_alt_Text](http://i.imgur.com/DPn5sP9.png)
### **Programmierbeispiel für Stamminformationen abrufen**
Der folgende Codeabschnitt ruft die Masterinformationen von diagram ab.


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

## **Fügen Sie Master aus der Schablone der Formen hinzu**
Eine Schablone ist eine Sammlung von Formen, die einer bestimmten Microsoft Office Visio Vorlage zugeordnet sind. Mit Aspose.Diagram ist es möglich, beliebige Shape-Master zu einer Zeichnung aus einer Schablone hinzuzufügen.
### **Meister hinzufügen**
Das Master-Objekt stellt den Master eines Shape-Objekts in einem diagram dar. Die AddMaster-Methode, die von der Diagram-Klasse verfügbar gemacht wird, ermöglicht das Hinzufügen eines Masters aus einer Schablone. Es bietet die folgenden vier Möglichkeiten:

- Pfad der Schablonendatei und Master-ID.
- Dateipfad und Mastername der Schablone.
- Schablonendateistream und Master-ID.
- Schablonendateistream und Mastername.
- Master zu diagram aus Quelle diagram hinzufügen
#### **Master-Programmierbeispiel hinzufügen**

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

## **Master von Grund auf neu erstellen**
Aspose.Diagram API ermöglicht die Erstellung eines Masters von Grund auf ohne Schablone, Zeichnung oder Vorlage. Entwickler können die Erstellung von Master anpassen. Die Methode addMaster, die von der Klasse Diagram verfügbar gemacht wird, ermöglicht das Hinzufügen eines Masters.
#### **Master-Programmierbeispiel erstellen**

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

## **Holen Sie sich einen Master aus der Datei Visio**
Manchmal müssen Entwickler die Details des Masters einer Visio-Zeichnung abrufen. Die Aspose.Diagram API unterstützt diese Funktion.

 Aspose.Diagram for Java bietet die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)Klasse, die eine Visio-Zeichnung darstellt. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um die Details eines bestimmten Masters abzurufen. Die Klasse MasterCollection macht die Methoden GetMasterByName und GetMaster verfügbar, die aufgerufen werden können, um ein Master-Objekt abzurufen.
### **Abrufen eines Master-Objekts nach ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetMaster-Methode der Diagram.Masters-Klasse auf.
#### **Programmierbeispiel für Master-Objekt nach ID**
Das folgende Beispiel zeigt, wie Sie einen Master nach ID aus einer Visio-Zeichnung erhalten.


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

### **Abrufen eines Master-Objekts nach Namen**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetMasterByName-Methode der Diagram.Masters-Klasse auf.
#### **Master Object by Name Programmierbeispiel**
Das folgende Beispiel zeigt, wie Sie ein Master-Objekt anhand des Namens aus einer Visio-Zeichnung abrufen.


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

## **Überprüfen Sie das Vorhandensein eines Masters in der Visio-Zeichnung**
Die Aspose.Diagram API unterstützt die Überprüfung auf das Vorhandensein eines Masters in einer Visio-Zeichnung. Mit der MasterCollection-Eigenschaft können Entwickler anhand ihres Namens oder ihrer ID prüfen, ob ein Master vorhanden ist.

 Aspose.Diagram for Java bietet die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um das Vorhandensein eines bestimmten Masters zu überprüfen. Die MasterCollection-Klasse macht die IsExist-Methode verfügbar, die mit dem Masternamen- oder ID-Parameter aufgerufen werden kann.
### **Überprüfen einer Master-Anwesenheit anhand der ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die IsExist-Methode der Diagram.Masters-Klasse auf.
#### **Master Presence by ID Programmierbeispiel**
Das folgende Beispiel zeigt, wie das Vorhandensein eines Masters anhand der ID in einer Visio-Zeichnung überprüft wird.


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

### **Überprüfen einer Master-Anwesenheit anhand des Namens**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die IsExist-Methode der Diagram.Masters-Klasse auf.
#### **Master Presence by Name Programmierbeispiel**
Das folgende Beispiel zeigt, wie eine Master-Anwesenheit anhand des Namens aus der Zeichnung Visio überprüft wird.


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

