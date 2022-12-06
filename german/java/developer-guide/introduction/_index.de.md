﻿---
title: Einführung
type: docs
weight: 10
url: /de/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio speichert Informationen über Aktionen, die an einem diagram in der Datei durchgeführt wurden. Beispielsweise werden die Uhrzeit und das Datum der Erstellung des Dokuments, der letzten Bearbeitung, des Drucks oder der Speicherung mit der Datei gespeichert. Außerdem wird gespeichert, mit welcher Version von Microsoft Visio die Datei erstellt und zuletzt bearbeitet wurde.

In diesem Artikel wird erläutert, wie Sie diese Informationen abrufen.

{{% /alert %}} 
## **Holen Sie sich die Version der Aspose.Diagram for Java Bibliothek**
 Die Methode getVersion(), die von der bereitgestellt wird[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) -Klasse und die getBuildNumberCreated() -Methode, die von der bereitgestellt werden[Dokumenteigenschaften](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) -Klasse werden verwendet, um die Version und die vollständige Build-Nummer der Instanz Microsoft Visio zu ermitteln, die zum Erstellen des Dokuments verwendet wurde.
### **Bestimmen der Version von Microsoft Visio, die ein Dokument erstellt, bearbeitet und gespeichert hat**
 Die Methode getBuildNumberEdited(), die von der bereitgestellt wird[Dokumenteigenschaften](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) -Klasse wird verwendet, um die vollständige Build-Nummer der Instanz Microsoft Visio zu ermitteln, die zum Bearbeiten des Dokuments verwendet wird.

Die Methoden getTimeCreated(), getTimeEdited(), getTimePrinted() und getTimeSaved(), die von der bereitgestellt werden[Dokumenteigenschaften](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) -Klasse werden verwendet, um den Zeitpunkt zu bestimmen, zu dem das Dokument Microsoft Visio erstellt, zuletzt bearbeitet, zuletzt gedruckt und zuletzt gespeichert wurde.

Sie können diese Eigenschaften auch festlegen, um die Informationen in der Datei zu ändern.

Die folgenden Codebeispiele zeigen, wie Sie Informationen darüber abrufen, was die Datei erstellt hat und wann sie erstellt, bearbeitet, gedruckt und gespeichert wurde.

**Die Codeausgabe in einem Konsolenfenster** 

![todo: Bild_alt_Text](introduction_1.png)
#### **Programmierbeispiel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-GetLibraryVersion-GetLibraryVersion.java" >}}
## **Schreiben Microsoft Visio Document Summary Info**
Mit Microsoft Visio können Sie eine Reihe von zusammenfassenden Informationseigenschaften für Dokumente definieren, die Ihnen und Ihren Kollegen helfen, eine diagram zu identifizieren. Zusammenfassende Eigenschaften, z. B. Titel, Betreff, Autor und Beschreibung, erleichtern das Auffinden der Datei bei der Suche und die Erkennung beim Durchsuchen Dateien.

 Das[Dokumenteigenschaften](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)-Klasse stellt eine Reihe von Eigenschaften bereit, um die zusammenfassenden Informationen von Microsoft Visio diagram festzulegen oder abzurufen. Aspose.Diagram for Java kann die Zeichnungszusammenfassungsinformationen aktualisieren und dann die Zeichnungsdatei zurück zu VDX schreiben.

{{% alert color="primary" %}} 

Bitte beachten Sie, dass Sie keine Werte gegen die setzen können**Anwendung**und**Hersteller**Felder, da Aspose Ltd. und Aspose.Diagram for Java xxx neben diesen Feldern angezeigt werden.

{{% /alert %}} 
### **Schreiben Microsoft Visio Document Summary Info**
So aktualisieren Sie die Zeichnungszusammenfassungsinformationen einer vorhandenen VDX- oder VSD-Datei:

1.  Erstellen Sie eine Instanz der[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) Klasse.
1. Legen Sie Eigenschaften fest, die von der Methode Diagram.getDocumentProps() bereitgestellt werden, um die zusammenfassenden Informationen für die Zeichnungsdatei Visio zu definieren.
1. Rufen Sie die Methode save() der Klasse Diagram auf, um die Zeichnungsdatei Visio in VDX zu schreiben.

Überprüfen Sie die zusammenfassenden Informationen:

1. Öffnen Sie die Ausgabedatei VDX in Microsoft Visio.
1.  Auswählen**Die Info** von dem**Datei** Speisekarte.

**Das Info-Dialogfeld mit den aktualisierten zusammenfassenden Informationen** 

![todo: Bild_alt_Text](introduction_2.png)
#### **Programmierbeispiel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-SetVisioProperties-SetVisioProperties.java" >}}
## **Erkennen Sie das Format einer Visio-Datei**
 Verwenden[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API können Entwickler das Format der Datei Visio vor dem Öffnen erkennen, da die Dateierweiterung nicht garantiert, dass der Dateiinhalt angemessen ist.
### **Programmierbeispiel für Erkennungsformat**
Der folgende Beispielcode veranschaulicht, wie ein Dateiformat (unter Verwendung des Dateipfads oder Streams) erkannt und seine Erweiterung überprüft wird.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.java" >}}
## **Erkennen Sie das Format einer Visio-Datei aus einem InputStream**
Mit Aspose.Diagram for Java API können Entwickler das Format einer Visio-Datei erkennen, indem sie einen Eingabestrom übergeben. Dazu kann die Methode detectFileFormat der Klasse FileFormatUtil verwendet werden.
### **Format aus einem InputStream-Programmierbeispiel erkennen**
Der folgende Beispielcode veranschaulicht, wie ein Dateiformat mithilfe eines Eingabestreams erkannt wird.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}
