---
title: Travailler avec les maîtres
type: docs
weight: 30
url: /fr/java/working-with-masters/
---
## **Récupération des informations sur le maître**
Un maître de forme est un autre nom pour un gabarit Visio. Avec Aspose.Diagram, il est possible de récupérer des informations sur les pages, les connecteurs, mais aussi les masters. Cet article explique comment obtenir l'ID et le nom d'un diagram.

 La[Maître](https://reference.aspose.com/diagram/java/com.aspose.diagram/master) l'objet représente un[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)maître de l'objet dans un diagram. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour récupérer les informations des maîtres, c'est-à-dire l'ID et le nom du maître.

Utilisez la propriété Page.Shapes pour déterminer quelle forme a été héritée par la forme de base.

**Une fenêtre de console affichant la sortie du code.** 

![tâche : image_autre_texte](http://i.imgur.com/DPn5sP9.png)
### **Récupération de l'exemple de programmation des informations principales**
Le morceau de code suivant récupère les informations des maîtres à partir d'un diagram.


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

## **Ajouter un maître à partir du gabarit de formes**
Un gabarit est une collection de formes associées à un gabarit particulier. Avec Aspose.Diagram, il est possible d'ajouter n'importe quel maître de forme à un dessin à partir d'un pochoir.
### **Ajouter maître**
L'objet Master représente le maître d'un objet Shape dans un diagram. La méthode AddMaster, exposée par la classe Diagram, permet d'ajouter un maître à partir d'un gabarit. Il propose les quatre manières suivantes :

- Chemin d'accès au fichier Stencil et ID principal.
- Chemin d'accès au fichier Stencil et nom du masque.
- Flux de fichiers Stencil et ID maître.
- Flux de fichier Stencil et nom du maître.
- Ajouter le maître à diagram à partir de la source diagram
#### **Ajouter un exemple de programmation maître**

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

## **Créer un maître à partir de zéro**
Aspose.Diagram API permet de créer un Master à partir de zéro sans aucun pochoir, dessin ou modèle. Les développeurs peuvent personnaliser la création de Master. La méthode addMaster, exposée par la classe Diagram, permet d'ajouter un maître.
#### **Créer un exemple de programmation maître**

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

## **Obtenir un Master à partir du fichier Visio**
Parfois, les développeurs ont besoin d'obtenir les détails d'un maître de dessin Visio. Le Aspose.Diagram API prend en charge cette fonctionnalité.

 Aspose.Diagram for Java offre le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)classe qui représente un dessin Visio. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour récupérer les détails d'un maître particulier. La classe MasterCollection expose les méthodes GetMasterByName et GetMaster qui peuvent être appelées pour obtenir un objet Master.
### **Obtenir un objet principal par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetMaster de la classe Diagram.Masters.
#### **Exemple de programmation d'objet maître par ID**
L'exemple suivant montre comment obtenir une forme de base par ID à partir d'un dessin Visio.


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

### **Obtenir un objet principal par nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetMasterByName de la classe Diagram.Masters.
#### **Exemple de programmation d'objet maître par nom**
L'exemple suivant montre comment obtenir un objet principal par son nom à partir d'un dessin Visio.


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

## **Vérifier la présence d'un maître dans le dessin Visio**
Le Aspose.Diagram API prend en charge la vérification de la présence d'un maître dans un dessin Visio. Avec la propriété MasterCollection, les développeurs peuvent vérifier si un maître est présent par son nom ou son ID.

 Aspose.Diagram for Java offre le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe qui représente un dessin Visio. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour vérifier la présence d'un maître particulier. La classe MasterCollection expose la méthode IsExist qui peut être appelée avec le nom principal ou le paramètre ID.
### **Vérifier la présence d'un maître par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode IsExist de la classe Diagram.Masters.
#### **Présence principale par exemple de programmation ID**
L'exemple suivant montre comment vérifier la présence d'un maître par ID dans un dessin Visio.


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

### **Vérifier la présence d'un maître par son nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode IsExist de la classe Diagram.Masters.
#### **Exemple de programmation de présence principale par nom**
L'exemple suivant montre comment vérifier la présence d'un maître par son nom à partir du dessin Visio.


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

