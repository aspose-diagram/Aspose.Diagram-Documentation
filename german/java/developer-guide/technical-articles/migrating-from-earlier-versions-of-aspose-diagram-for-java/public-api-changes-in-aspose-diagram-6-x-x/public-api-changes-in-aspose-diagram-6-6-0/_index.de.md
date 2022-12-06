---
title: Öffentlich API Änderungen in Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /de/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.3.0 auf 6.6.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Fügt die Formate VSDM, VSSM und VSTM in der LoadFileFormat-Klasse hinzu**
Diese Version fügt Unterstützung für das Lesen von makrofähigen Visio-Formaten hinzu.
### **Fügt die Formate VSDM, VSSM und VSTM in der SaveFileFormat-Klasse hinzu**
Diese Version fügt Unterstützung für das Schreiben von makrofähigen Visio-Formaten hinzu.
### **Ändern Sie den VBA-Modulcode in Visio Diagram**
Wir haben die Klassen Vba, VbaProject und VbaModule hinzugefügt. Diese Klassen helfen dabei, die Kontrolle über das VBA-Projekt zu erlangen. Mit dieser neuen Version 6.6.0 oder höher können Entwickler VBA-Modulcode extrahieren und ändern. Bitte überprüfen Sie dieses Codebeispiel:

**Java**

{{< highlight "java" >}}

 // lade eine vorhandene Visio diagram

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = neu Diagram (Eingang);

// VBA-Projekt extrahieren

VbaProject v = diagram.getVbaProject();

// Die Module durchlaufen und den VBA-Makrocode ändern

für (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

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
### **Fügt eine getImageData-Methode in der ForeignData-Klasse hinzu**
Es stellt ein Bild eines Ole-Objekts als Byte-Array dar. Außerdem haben wir die Manipulation von OLE-Objekten verbessert. Entwickler können jetzt auch ein OLE-Objekt in der Visio diagram ersetzen. Bitte überprüfen Sie dieses Codebeispiel:

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
