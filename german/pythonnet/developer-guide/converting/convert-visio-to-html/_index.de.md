---
title:  Konvertieren Sie Visio in das HTML-Format
linktitle: Konvertieren Sie Visio in HTML
type: docs
weight: 30
url: /de/python-net/convert-visio-to-html/
description: Dieses Thema zeigt Ihnen, wie Sie mit Aspose.Diagram Visio in HTML-Formate konvertieren können. Konvertieren Sie VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in HTML mit ein paar Zeilen Code.
---
## **Visio in HTML exportieren**
 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in HTML exportieren[Aspose.Diagram für Python über .NET](https://products.aspose.com/diagram/python-net/) API.

Verwenden Sie den Klassenkonstruktor Diagram, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren. Entwickler können den resultierenden HTML-Code im lokalen Speicher oder direkt in einer Stream-Instanz speichern.

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
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
