---
title:  Konvertieren Sie Visio in das HTML-Format
linktitle: Konvertieren Sie Visio in HTML
type: docs
weight: 30
url: /de/java/convert-visio-to-html/
description: Dieses Thema zeigt Ihnen, wie Sie mit Aspose.Diagram Visio in HTML-Formate konvertieren können. Konvertieren Sie VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in HTML mit ein paar Zeilen Code.
---
## **Visio in HTML exportieren** **Visio in HTML exportieren**
 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in HTML exportieren[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Verwenden Sie die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) -Klassenkonstruktor zum Lesen der diagram-Dateien und die Save-Methode zum Exportieren von diagram in ein beliebiges unterstütztes Bildformat. Entwickler können den resultierenden HTML-Code im lokalen Speicher oder direkt in einer Stream-Instanz speichern.

1. [Speichern Sie das resultierende HTML im lokalen Speicher](/diagram/de/java/how-to-convert-a-visio-diagram/).
1. [Speichern Sie den resultierenden HTML-Code in einer Stream-Instanz](/diagram/de/java/how-to-convert-a-visio-diagram/).

Das Bild unten zeigt eine VSD-Datei, die im PNG-Format gespeichert werden soll. Sie können auch andere diagram-Formate (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX oder 07611)1 verwenden.

**Geben Sie diagram ein.**

![todo: Bild_alt_Text](http://i.imgur.com/YX4BNNq.png)

Um VSD diagram in HTML zu exportieren, führen Sie die folgenden Schritte aus:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Dagram-Klasse auf und legen Sie HTML als Ausgabeformat fest.

Das folgende Bild zeigt die ausgegebene HTML-Datei.

**Ausgabe-HTML diagram.**

![todo: Bild_alt_Text](http://i.imgur.com/syavUqI.png)
### **Speichern Sie das resultierende HTML im lokalen Speicher**
Die resultierende Datei kann gespeichert werden, indem ein vollständiger Pfad-String einschließlich des Dateinamens und der Erweiterung übergeben wird, z. B. @"c:\temp\MyOutput.html".
#### **Speichern des resultierenden HTML-Codes im Programmierbeispiel für lokalen Speicher**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Speichern Sie den resultierenden HTML-Code in einer Stream-Instanz**
Es ist ein Anwendungsfall, um das resultierende HTML in einer Datenbank oder einem Repository zu speichern, ohne es im lokalen Speicher zu speichern. Diese Funktion bettet auch andere resultierende Ressourcen des HTML ein, z. B. Schriftarten, CSS (die die Stilinformationen enthalten) und Bilder. Da es eine einzelne HTML-Datei in der Stream-Instanz speichert.
#### **Speichern Sie den resultierenden HTML-Code in einem Stream-Programmierbeispiel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
