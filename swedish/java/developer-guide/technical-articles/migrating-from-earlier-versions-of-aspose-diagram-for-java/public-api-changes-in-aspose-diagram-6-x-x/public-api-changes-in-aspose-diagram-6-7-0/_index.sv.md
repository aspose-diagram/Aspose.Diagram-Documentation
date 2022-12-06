---
title: Offentlig API Ändringar i Aspose.Diagram 6.7.0
type: docs
weight: 20
url: /sv/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 6.6.0 till 6.7.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **Lägger till metoden detectFileFormat i klassen FileFormatUtil**
Den upptäcker och returnerar information om formatet för en lagrad Visio diagram i en ingångsström. Kontrollera detta kodexempel:

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
