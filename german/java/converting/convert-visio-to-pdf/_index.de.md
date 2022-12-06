---
title:  Konvertieren Sie Visio in das PDF-Format
linktitle: Konvertieren Sie Visio in PDF
type: docs
weight: 10
url: /de/java/convert-visio-to-pdf/
description: In diesem Thema erfahren Sie, wie Sie mit Aspose.Diagram Visio in PDF-Formate konvertieren können. Konvertieren Sie VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in PDF mit ein paar Zeilen Code.
---
## **Exportieren in PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java schreibt die Informationen über API und Versionsnummer direkt in Ausgabedokumente. Beim Rendern einer Zeichnung in PDF wird beispielsweise Aspose.Diagram for Java ausgefüllt**Anwendung**Feld mit dem Wert 'Aspose.Diagram' und**PDF-Produzent**Feld mit einem Wert, zB 'Aspose.Diagram 17.9'.

Bitte beachten Sie, dass Sie Aspose.Diagram for Java API nicht anweisen können, diese Informationen aus Ausgabedokumenten zu ändern oder zu entfernen.

{{% /alert %}}

 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram als PDF exportieren[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Verwenden Sie die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

Das Bild unten zeigt die VSD diagram, die die Codeschnipsel unten als PDF exportieren. Sie können auch andere diagram-Formate (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX oder VSX) verwenden.

**Die Quelldatei.**

![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_1.png)

VSD diagram als PDF exportieren:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse Diagram auf und legen Sie das Ausgabeformat auf PDF fest.

Unten sehen Sie ein Bild der ausgegebenen PDF-Datei.

**Die ausgegebene PDF-Datei.**

![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_2.png)
### **Exportieren in ein PDF-Programmierbeispiel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Mehrere Seiten aufteilen**
Aspose.Diagram for Java ermöglicht das Aufteilen mehrerer Seiten beim Konvertieren von Microsoft Visio Diagram in PDF. Das folgende Code-Snippet zeigt die Funktionalität.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Verwenden Sie den Seitenspeicher-Callback**
Falls Sie mehrere Seiten haben, ermöglicht Aspose.Diagram for Java die Verwendung des Rückrufs zum Speichern von Seiten, während Microsoft Visio Diagram in PDF konvertiert wird. Das folgende Code-Snippet zeigt die Funktionalität.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **TestDiagramPageSavingCallback-Klasse**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
