---
title:  Konvertieren Sie Visio in das PDF-Format
linktitle: Konvertieren Sie Visio in PDF
type: docs
weight: 10
url: /de/python-java/convert-visio-to-pdf/
description: Dieses Thema zeigt Ihnen, wie Sie Visio in PDF -Formate unter Verwendung Aspose.Diagram für Python über Java konvertieren.
---
## **Exportieren in PDF**
{{% alert color="primary" %}}

Aspose.Diagram für Python über Java schreibt die Informationen über API und Versionsnummer direkt in Ausgabedokumente. Beim Rendern einer Zeichnung in PDF wird beispielsweise Aspose.Diagram for Java ausgefüllt**Anwendung**Feld mit dem Wert 'Aspose.Diagram' und**PDF-Produzent**Feld mit einem Wert, zB 'Aspose.Diagram 17.9'.

Bitte beachten Sie, dass Sie Aspose.Diagram nicht für Python über Java anweisen können, diese Informationen aus Ausgabedokumenten zu ändern oder zu entfernen.

{{% /alert %}}

In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in PDF exportieren, indem Sie Aspose.Diagram für Python über Java verwenden.

Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

[Die VSD diagram](ExportToPDF.vsd) ist die Beispielzeichnungsdatei zum Exportieren von PDF. Sie können auch andere diagram-Formate (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX oder VSX) verwenden.

VSD diagram als PDF exportieren:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse Diagram auf und legen Sie das Ausgabeformat auf PDF fest.

### **Exportieren in ein PDF-Programmierbeispiel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Mehrere Seiten aufteilen**
Aspose.Diagram for Java ermöglicht das Aufteilen mehrerer Seiten beim Konvertieren von Microsoft Visio Diagram in PDF. Das folgende Code-Snippet zeigt die Funktionalität.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
