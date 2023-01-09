---
title: Einführung
type: docs
weight: 10
url: /de/net/introduction/
description: Einführung der Bibliothek Aspose.Diagram.
---
## **Holen Sie sich die Visio Dokumentinformationen der Aspose.Diagram for .NET Bibliothek**
Microsoft Visio speichert Informationen über Aktionen, die an einem diagram in der Datei durchgeführt wurden. Beispielsweise werden die Uhrzeit und das Datum der Erstellung des Dokuments, der letzten Bearbeitung, des Drucks oder der Speicherung mit der Datei gespeichert. Außerdem wird gespeichert, mit welcher Version von Microsoft Visio die Datei erstellt und zuletzt bearbeitet wurde.

In diesem Artikel wird erläutert, wie Sie diese Informationen abrufen.
### **Bestimmen der Version von Microsoft Visio, die ein Dokument erstellt, bearbeitet und gespeichert hat**
 Die Version-Eigenschaft, die von der bereitgestellt wird[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)-Klasse und die BuildNumberCreated-Eigenschaft, die von der DocumentProperties-Klasse verfügbar gemacht wird, wird verwendet, um die Version und die vollständige Build-Nummer der Microsoft Visio-Instanz zu bestimmen, die zum Erstellen des Dokuments verwendet wurde.

 Die BuildNumberEdited-Eigenschaft, die von der bereitgestellt wird[Dokumenteigenschaften](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) -Klasse wird verwendet, um die vollständige Build-Nummer der Instanz Microsoft Visio zu ermitteln, die zum Bearbeiten des Dokuments verwendet wird.

Die von der DocumentProperties-Klasse bereitgestellten Eigenschaften TimeCreated, TimeEdited, TimePrinted und TimeSaved werden verwendet, um die Zeit zu bestimmen, zu der das Dokument Microsoft Visio erstellt, zuletzt bearbeitet, zuletzt gedruckt und zuletzt gespeichert wurde.

Sie können diese Eigenschaften auch festlegen, um die Informationen in der Datei zu ändern. Die folgenden Codebeispiele zeigen, wie Sie Informationen darüber abrufen, was die Datei erstellt hat und wann sie erstellt, bearbeitet, gedruckt und gespeichert wurde.
#### **Programmierbeispiel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Schreiben von Visio Dokumentzusammenfassungsinformationen**
Mit Microsoft Visio können Sie eine Reihe von zusammenfassenden Informationseigenschaften für Dokumente definieren, die Ihnen und Ihren Kollegen helfen, eine diagram zu identifizieren. Zusammenfassende Eigenschaften, z. B. Titel, Betreff, Autor und Beschreibung, machen die Datei bei der Suche leichter zu finden und leichter zu erkennen, wann Durchsuchen von Dateien.
### **Schreiben Microsoft Visio Document Summary Info**
Die DocumentProperties-Klasse stellt eine Reihe von Eigenschaften bereit, um die zusammenfassenden Informationen von Microsoft Visio diagram festzulegen oder abzurufen. Aspose.Diagram for .NET kann die Zeichnungszusammenfassungsinformationen aktualisieren und dann die Zeichnungsdatei zurück zu VDX schreiben.

{{% alert color="primary" %}} 

Bitte beachten Sie, dass Sie keine Werte gegen die setzen können**Anwendung**und**Hersteller**Felder, da Aspose Ltd. und Aspose.Diagram for .NET xxx neben diesen Feldern angezeigt werden.

{{% /alert %}} 

So aktualisieren Sie die Zeichnungszusammenfassungsinformationen einer vorhandenen VDX- oder VSD-Datei:

1.  Erstellen Sie eine Instanz der[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) Klasse.
1.  Legen Sie die Eigenschaften fest, die von bereitgestellt werden[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) um die zusammenfassenden Informationen für die Zeichnungsdatei Visio zu definieren.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VDX zu schreiben.

Überprüfen Sie die zusammenfassenden Informationen:

1. Öffnen Sie die Ausgabedatei VDX in Microsoft Visio.
1. Wählen Sie Info aus dem Menü Datei.
#### **Writing Visio Document Summary Information Programmierbeispiel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Erkennen Sie das Format der Datei Visio**
Mit Aspose.Diagram for .NET API können Entwickler das Format der Visio-Datei vor dem Öffnen erkennen, da die Dateierweiterung nicht garantiert, dass der Dateiinhalt angemessen ist.
### **Programmierbeispiel für Erkennungsformat**
Der folgende Beispielcode veranschaulicht, wie ein Dateiformat (unter Verwendung des Dateipfads oder Streams) erkannt und seine Erweiterung überprüft wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
