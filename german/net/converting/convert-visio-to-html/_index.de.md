---
title:  Konvertieren Sie Visio in das HTML-Format
linktitle: Konvertieren Sie Visio in HTML
type: docs
weight: 30
url: /de/net/convert-visio-to-html/
description: Dieses Thema zeigt Ihnen, wie Sie mit Aspose.Diagram Visio in HTML-Formate konvertieren können. Konvertieren Sie VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in HTML mit ein paar Zeilen Code.
---
## **Visio in HTML exportieren**
 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in HTML exportieren[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Verwenden Sie die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) -Klassenkonstruktor zum Lesen der diagram-Dateien und die Save-Methode zum Exportieren von diagram in ein beliebiges unterstütztes Bildformat. Entwickler können den resultierenden HTML-Code im lokalen Speicher oder direkt in einer Stream-Instanz speichern.

1. [Speichern Sie das resultierende HTML im lokalen Speicher](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Speichern Sie den resultierenden HTML-Code in einer Stream-Instanz](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

Das Bild unten zeigt eine VSD-Datei, die im PNG-Format gespeichert werden soll. Sie können auch andere diagram-Formate (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX oder 07611)1 verwenden.

|**Geben Sie diagram ein.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_6.png)|
Um VSD diagram in HTML zu exportieren, führen Sie die folgenden Schritte aus:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Dagram-Klasse auf und legen Sie HTML als Ausgabeformat fest.
### **Speichern Sie das resultierende HTML im lokalen Speicher**
Die resultierende Datei kann gespeichert werden, indem ein vollständiger Pfad-String einschließlich des Dateinamens und der Erweiterung übergeben wird, z. B. @"c:\temp\MyOutput.html".
#### **Speichern des resultierenden HTML-Codes im Programmierbeispiel für lokalen Speicher**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToHTML-ExportToHTML.cs" >}}



### **Speichern Sie den resultierenden HTML-Code in einer Stream-Instanz**
Es ist ein Anwendungsfall, um das resultierende HTML in einer Datenbank oder einem Repository zu speichern, ohne es im lokalen Speicher zu speichern. Diese Funktion bettet auch andere resultierende Ressourcen des HTML ein, z. B. Schriftarten, CSS (die die Stilinformationen enthalten) und Bilder. Da es eine einzelne HTML-Datei in der Stream-Instanz speichert.
#### **Speichern Sie den resultierenden HTML-Code in einem Stream-Programmierbeispiel**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
