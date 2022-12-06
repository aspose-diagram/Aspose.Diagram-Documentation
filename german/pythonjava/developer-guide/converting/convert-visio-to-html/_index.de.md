---
title:  Konvertieren Sie Visio in das HTML-Format
linktitle: Konvertieren Sie Visio in HTML
type: docs
weight: 30
url: /de/python-java/convert-visio-to-html/
description: Dieses Thema zeigt Ihnen, wie Sie Visio in HTML -Formate unter Verwendung Aspose.Diagram für Python über Java konvertieren.
---
## **Visio in HTML exportieren** ##
 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in HTML exportieren[Aspose.Diagram für Python über Java](https://products.aspose.com/diagram/python-java/) API.

Verwenden Sie den Klassenkonstruktor Diagram, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren. Entwickler können den resultierenden HTML-Code im lokalen Speicher oder direkt in einer Stream-Instanz speichern.

 Das Bild unten zeigt a[VSD Datei](ExportToHTML.vsd)im PNG-Format gespeichert werden. Sie können auch andere diagram-Formate verwenden (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX oder 076110).

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
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **Speichern Sie den resultierenden HTML-Code in einer Stream-Instanz**
Es ist ein Anwendungsfall, um das resultierende HTML in einer Datenbank oder einem Repository zu speichern, ohne es im lokalen Speicher zu speichern. Diese Funktion bettet auch andere resultierende Ressourcen des HTML ein, z. B. Schriftarten, CSS (die die Stilinformationen enthalten) und Bilder. Da es eine einzelne HTML-Datei in der Stream-Instanz speichert.
#### **Speichern Sie den resultierenden HTML-Code in einem Stream-Programmierbeispiel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
