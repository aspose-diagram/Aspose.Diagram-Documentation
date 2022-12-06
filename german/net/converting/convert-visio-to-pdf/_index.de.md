---
title:  Konvertieren Sie Visio in das PDF-Format
linktitle: Konvertieren Sie Visio in PDF
type: docs
weight: 10
url: /de/net/convert-visio-to-pdf/
description: In diesem Thema erfahren Sie, wie Sie mit Aspose.Diagram Visio in PDF-Formate konvertieren können. Konvertieren Sie VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in PDF mit ein paar Zeilen Code.
---
## **Als PDF exportieren**
{{% alert color="primary" %}}

Aspose.Diagram for .NET schreibt die Informationen über API und Versionsnummer direkt in Ausgabedokumente. Beim Rendern einer Zeichnung in PDF wird beispielsweise Aspose.Diagram for .NET ausgefüllt**Anwendung** Feld mit dem Wert 'Aspose.Diagram' und**PDF-Produzent** Feld mit Wert, zB 'Aspose.Diagram 17.9'.

Bitte beachten Sie, dass Sie Aspose.Diagram for .NET API nicht anweisen können, diese Informationen aus Ausgabedokumenten zu ändern oder zu entfernen.

{{% /alert %}}

 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram als PDF exportieren[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Verwenden Sie die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) -Klassenkonstruktor zum Lesen der diagram-Dateien und die Save-Methode zum Exportieren von diagram in ein beliebiges unterstütztes Bildformat.

Das Bild unten zeigt die VSD diagram, die die Codeschnipsel unten als PDF exportieren. Sie können auch andere diagram-Formate (VSS, VSSM, VDX, VST, VSTX, VDX, VTX oder VSX) verwenden.

|**Die Quelldatei.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_1.png)|


VSD diagram als PDF exportieren:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse Diagram auf und legen Sie das Ausgabeformat auf PDF fest.

Unten sehen Sie ein Bild der ausgegebenen PDF-Datei.

|**Die ausgegebene PDF-Datei.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_2.png)|
### **Microsoft Visio Zeichnung in PDF exportieren**
Die Codebeispiele zeigen, wie Sie Microsoft Visio Drawing mit C# in PDF exportieren.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Mehrere Seiten aufteilen**
Aspose.Diagram for .NET ermöglicht das Aufteilen mehrerer Seiten beim Konvertieren von Microsoft Visio Diagram in PDF. Das folgende Code-Snippet zeigt die Funktionalität.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Verwenden Sie den Seitenspeicher-Callback**
Falls Sie mehrere Seiten haben, ermöglicht Aspose.Diagram for .NET die Verwendung des Rückrufs zum Speichern von Seiten, während Microsoft Visio Diagram in PDF konvertiert wird. Das folgende Code-Snippet zeigt die Funktionalität.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **TestDiagramPageSavingCallback-Klasse**
{{< highlight "java" >}}

 öffentliche Klasse TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{  public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)  {  Console.WriteLine("Start save diagram page {0} of pages {1}", args.PageIndex + 1, args.Page0Count);  {   }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.WriteLine("Speicherung diagram Seite {0} von Seiten {1} beenden", args.PageIndex. + 1);   //don't output pages after page index 8.  if (args.PageIndex >= 8)  {  args.HasMorePages = false;  }  }  }
