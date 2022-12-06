---
title:  Konvertieren Sie Visio in Bildformate
linktitle: Konvertieren Sie Visio in Bilder
type: docs
weight: 20
url: /de/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a paar Zeilen Code.
---
## **Diagramme in Bilddateiformate exportieren**
In diesem Artikel wird erläutert, wie Sie ein Microsoft Visio diagram in ein Bild exportieren, indem Sie Aspose.Diagram für Python über Java verwenden.

Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um die diagram in ein beliebiges unterstütztes Bildformat zu exportieren. Das folgende Bild zeigt eine VSD-Datei, die im PNG-Format gespeichert werden soll. Sie können auch andere diagram-Formate (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX oder VSX) verwenden.

**[Die Beispieldatei VSD.](ExportToImage.vsd)**

So exportieren Sie eine diagram in ein Bild:

- Erstellen Sie eine Instanz der Klasse Diagram.
- Rufen Sie die Save-Methode der Diagram-Klasse auf und legen Sie das Bildformat fest, in das Sie exportieren möchten. Die Ausgabebilddatei sieht aus wie die Originaldatei.

**Die ausgegebene PNG-Datei.**

![todo: Bild_alt_Text](ExportToImage.png)
### **Exportieren in eine Bilddatei Programmierbeispiel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

Es ist auch möglich, anstelle des gesamten Dokuments eine bestimmte Seite als Bild zu speichern:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}