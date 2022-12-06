---
title: Öffentlich API Änderungen in Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /de/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 5.8.0 auf 5.9.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
### **Speichern Sie den resultierenden HTML-Code in einem Stream**
Die neue save-Methode wurde der Klasse Diagram hinzugefügt. Es benötigt zwei Parameter, das Stream-Objekt und das Speicherdateiformat.
Beispielcode:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **Kopieren Sie Designs und PageSheet von einem anderen Visio**
Die Klasse Diagram bietet die CopyTheme-Methode und die PageSheet-Klasse bietet die Copy-Methode an, um das Ziel des Kopierens einer Form und andere Manipulationsaufgaben zu erreichen.
 Beispielcodes:[Kopieren Sie Formen von einem vorhandenen Visio](/diagram/de/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **VSTX und VSSX Speicheroptionen werden im SaveFileFormat hinzugefügt**
Zuvor unterstützte Aspose.Diagram API das Lesen und Schreiben des VSDX-Formats, aber jetzt haben wir auch Unterstützung für das Schreiben von Diagrammen in den Formaten VSTX und VSSX hinzugefügt. Beispielcodes:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX Leseoption wird im LoadFileFormat hinzugefügt**
Zuvor hatte Aspose.Diagram API das Lesen und Schreiben des VSDX-Formats unterstützt, aber jetzt haben wir auch die Unterstützung des Lesens des VSSX-Schablonenformats hinzugefügt. Beispielcodes:

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
