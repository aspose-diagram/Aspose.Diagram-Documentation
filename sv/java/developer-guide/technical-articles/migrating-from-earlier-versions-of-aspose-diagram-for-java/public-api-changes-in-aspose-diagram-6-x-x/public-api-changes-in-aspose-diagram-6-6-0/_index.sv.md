---
title: Offentlig API Ändringar i Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /sv/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 6.3.0 till 6.6.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **Lägger till formaten VSDM, VSSM och VSTM i klassen LoadFileFormat**
Denna version lägger till stöd för läsning av makroaktiverade Visio-format.
### **Lägger till formaten VSDM, VSSM och VSTM i klassen SaveFileFormat**
Denna version lägger till stöd för att skriva makroaktiverade Visio-format.
### **Ändra VBA-modulkod i Visio Diagram**
Vi har lagt till klasser Vba, VbaProject och VbaModule. Dessa klasser hjälper till att få kontroll över VBA-projekt. Med den här nya versionen 6.6.0 eller senare kan utvecklare extrahera och modifiera VBA-modulkod. Kontrollera detta kodexempel:

**Java**

{{< highlight "java" >}}

 // ladda en befintlig Visio diagram

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = ny Diagram(ingång);

// extrahera VBA-projekt

VbaProject v = diagram.getVbaProject();

// Iterera genom modulerna och ändra VBA-makrokod

för (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **Lägger till en getImageData-metod i klassen ForeignData**
Den representerar en bild av ett objekt som en byte-array. Utöver detta har vi också förbättrat manipuleringen av OLE-objekt. Utvecklare kan nu även ersätta ett OLE-objekt i Visio diagram. Kontrollera detta kodexempel:

**Java**

{{< highlight "java" >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
