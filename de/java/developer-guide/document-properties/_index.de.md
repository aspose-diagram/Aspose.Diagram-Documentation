---
title: Dokumenteigenschaften verwalten
linktitle: Dokumenteigenschaften
type: docs
weight: 80
url: /de/java/document-properties/
aliases: [/java/document-properties/]
description: Dokumenteigenschaften von visio-Dateien verwalten.
---
## **Einführung**

Microsoft Visio bietet die Möglichkeit, Eigenschaften zu visio-Dateien hinzuzufügen. Diese Dokumenteigenschaften bieten nützliche Informationen und sind wie unten beschrieben in zwei Kategorien unterteilt.

- Systemdefinierte (eingebaute) Eigenschaften: Eingebaute Eigenschaften enthalten allgemeine Informationen über das Dokument wie Dokumenttitel, Autorenname, Dokumentstatistiken und so weiter.
- Benutzerdefinierte (benutzerdefinierte) Eigenschaften: Benutzerdefinierte Eigenschaften, die vom Endbenutzer in Form von Name-Wert-Paaren definiert werden.

{{% alert color="primary" %}}

Der wichtigste Punkt, den Sie über integrierte und benutzerdefinierte Eigenschaften wissen sollten, ist, dass auf integrierte Eigenschaften zugegriffen und diese geändert, aber nicht erstellt oder entfernt werden können. Es können jedoch benutzerdefinierte Eigenschaften erstellt und verwaltet werden.

{{% /alert %}}

## **Verwalten von Dokumenteigenschaften mit Microsoft Visio**

 Mit Microsoft Visio können Sie die Dokumenteigenschaften der Visio-Dateien im WYSIWYG-Verfahren verwalten. Bitte befolgen Sie die nachstehenden Schritte, um die zu öffnen**Eigenschaften** Dialog in Visio 2016.

1.  Von dem**Datei** Menü, auswählen**Die Info**.

|**Auswählen des Info-Menüs**|
|:- |
|![todo: Bild_alt_Text](managing-document-properties_1.png)|
1.  Klicke auf**Eigenschaften** Überschrift und wählen Sie "Erweiterte Eigenschaften".

|**Klicken Sie auf Erweiterte Eigenschaftenauswahl**|
|:- |
|![todo: Bild_alt_Text](managing-document-properties_2.png)|
1. Verwalten Sie die Dokumenteigenschaften der Datei.

|**Eigenschaftendialog**|
|:- |
|![todo: Bild_alt_Text](managing-document-properties_3.png)|
Im Eigenschaftendialog gibt es verschiedene Registerkarten wie Allgemein, Zusammenfassung, Statistik, Inhalt und Benutzerdefiniert. Jede Registerkarte hilft bei der Konfiguration verschiedener Arten von Informationen in Bezug auf die Datei. Die Registerkarte Benutzerdefiniert wird verwendet, um benutzerdefinierte Eigenschaften zu verwalten.

## **Arbeiten mit Dokumenteigenschaften mit Aspose.Diagram**

Entwickler können die Dokumenteigenschaften mithilfe der Aspose.Diagram-APIs dynamisch verwalten. Diese Funktion hilft den Entwicklern, nützliche Informationen zusammen mit der Datei zu speichern, z. B. wann die Datei empfangen, verarbeitet, mit einem Zeitstempel versehen wurde und so weiter.

{{% alert color="primary" %}}

Aspose.Diagram for Java schreibt die Informationen über API und die Versionsnummer direkt in Ausgabedokumente.

Bitte beachten Sie, dass Sie Aspose.Diagram for Java nicht anweisen können, diese Informationen aus Ausgabedokumenten zu ändern oder zu entfernen.

{{% /alert %}}

### **Zugriff auf Dokumenteigenschaften**

 Aspose.Diagram APIs unterstützen beide Arten von Dokumenteigenschaften, integrierte und benutzerdefinierte. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) Klasse repräsentiert eine Visio-Datei und, wie eine visio-Datei, die[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) Die Klasse kann mehrere Seiten enthalten, die jeweils durch die dargestellt werden[**Buchseite**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) Klasse, während die Sammlung von Seiten durch die dargestellt wird[**Seitensammlung**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection)Klasse.

 Verwenden Sie die[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram), um wie unten beschrieben auf die Dokumenteigenschaften der Datei zuzugreifen.

- Um auf integrierte Dokumenteigenschaften zuzugreifen, verwenden Sie[**diagram.DocumentProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/documentproperties).
-  Um auf benutzerdefinierte Dokumenteigenschaften zuzugreifen, verwenden Sie[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/CustomPropCollection).


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


### **Hinzufügen oder Entfernen von benutzerdefinierten Dokumenteigenschaften**

Wie wir bereits zu Beginn dieses Themas beschrieben haben, können Entwickler keine integrierten Eigenschaften hinzufügen oder entfernen, da diese Eigenschaften systemdefiniert sind, aber es ist möglich, benutzerdefinierte Eigenschaften hinzuzufügen oder zu entfernen, da diese benutzerdefiniert sind.

### **Hinzufügen von benutzerdefinierten Eigenschaften**

 Aspose.Diagram APIs haben die ausgesetzt[**Hinzufügen**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#add(com.aspose.diagram.CustomProp) ) Methode für die[**CustomPropCollection**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection)-Klasse, um der Sammlung benutzerdefinierte Eigenschaften hinzuzufügen.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


### **Benutzerdefinierte Eigenschaften entfernen**

 Um benutzerdefinierte Eigenschaften mit Aspose.Diagram zu entfernen, rufen Sie die an[**CustomPropCollection.Remove**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#remove(com.aspose.diagram.CustomProp))-Methode und übergeben Sie den Namen der zu entfernenden Dokumenteigenschaft.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}

