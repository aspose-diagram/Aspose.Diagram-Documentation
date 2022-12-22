---
title: Öffentlich API Änderungen in Aspose.Diagram 6.7.0
type: docs
weight: 20
url: /de/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.6.0 zu 6.7.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Fügt die Methode detectFileFormat in der Klasse FileFormatUtil hinzu**
Es erkennt und gibt die Informationen über das Format einer gespeicherten Visio diagram in einem Eingabestrom zurück. Bitte überprüfen Sie dieses Codebeispiel:

**Java**

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Open the stream. Read only access to load a Visio diagram.

InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

// detect file format using an input stream

FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format

System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
