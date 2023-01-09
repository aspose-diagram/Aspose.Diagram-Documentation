---
title:  Konvertieren Sie Visio in andere Formate
linktitle:  Konvertieren Sie Visio in andere Formate
type: docs
weight: 40
url: /de/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
**[A Microsoft Visio diagram soll exportiert werden.](ExportToXML.vsd)**

## **Exportieren nach XML**
This article explains how to export a Microsoft Visio diagram to XML using Aspose.Diagram for Python via Java.

- VDX definiert ein XML diagram.
- VTX definiert eine XML-Vorlage.
- VSX definiert eine XML-Schablone.

Die Konstruktoren der Diagram-Klasse lesen eine diagram und die Save-Methode wird verwendet, um eine diagram in einem anderen Dateiformat zu speichern oder zu exportieren. Die Codeausschnitte in diesem Artikel zeigen, wie Sie die Save-Methode verwenden, um eine Visio-Datei in den Formaten VDX, VTX und VSX zu speichern.

### **Exportieren von VSD zu VDX**
VDX ist ein schemabasiertes XML-Dateiformat, mit dem Sie Diagramme in einem Format speichern können, das andere Produkte als Microsoft Visio lesen können. Es ist ein nützliches Format zum Übertragen von Diagrammen zwischen Softwareanwendungen und zum Aufbewahren bearbeitbarer Daten.

So exportieren Sie eine VSD diagram in VDX:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VDX zu schreiben.

### **Exportieren von VSD bis VSX**
VSX ist ein XML-Format zum Definieren von Schablonen, den Grundobjekten, aus denen ein diagram aufgebaut ist. Wenn eine Visio-Datei in VSX konvertiert wird, werden nur die Schablonen exportiert.

So exportieren Sie eine VSD diagram in VSX:

- Erstellen Sie eine Instanz der Klasse Diagram.
- Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VSX zu schreiben.

Das folgende Bild zeigt die Ausgabedatei VSX. Beachten Sie, dass die in diagram verwendeten Schablonen, nicht diagram selbst, exportiert werden.

### **Exportieren Sie VSD bis VTX**
TVX ist eine XML-Darstellung einer Vorlagendatei und speichert die Einstellungen für das Dokument.

So exportieren Sie eine VSD diagram in VTX:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse diagram auf, um die Zeichnungsdatei Visio im Format VTX zu schreiben.

Das folgende Bild zeigt die Ausgabedatei VTX.

### **Exportieren in ein XML-Programmierbeispiel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXML.py" >}}

## **Exporting to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using Aspose.Diagram for Python via Java.
Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

To export VSD diagram to XPS:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.

Das folgende Bild zeigt die Ausgabedatei XPS.

### **Exporting to XPS Programming Sample**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **Exporting a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using Aspose.Diagram for Python via Java.

Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

To export VSD diagram to SVG, perform the following steps:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the class' Save method and set SVG as the export format.

### **Exporting Diagram to SVG Programming Sample**
The code samples show how to export a diagram to SVG using Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **Exporting a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using Aspose.Diagram for Python via Java.

Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

So exportieren Sie eine VSD diagram in XAML:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the class' Save method and set XAML as the export format.

### **Exporting to XAML Programming Sample**
The code sample show how to export a diagram to XAML using Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXAML.py" >}}

## **Konvertieren Visio Zeichnen mit ausgewählten Formen**
Mit Aspose.Diagram API können Entwickler eine Gruppe von Formen auswählen, um eine Visio-Zeichnung in ein beliebiges anderes unterstütztes Format zu konvertieren. Die RenderingSaveOptions-Klasse bietet ein Shapes-Member, um die Gruppe von Formen zu verwalten. Jede Speicheroptionsklasse ist die erweiterte Form der RenderingSaveOptions-Klasse.

So exportieren Sie eine Visio-Zeichnung mit ausgewählten Formen:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz einer beliebigen SaveOption-Klasse, um Einstellungen wie kommentiert anzugeben
1. Rufen Sie die Methode save des Klassenobjekts Diagram auf und übergeben Sie das Klassenobjekt save option als Parameter.

### **Konvertieren Visio Programmierbeispiel für Zeichnen mit ausgewählten Formen**
Das Codebeispiel zeigt, wie eine Zeichnung mit ausgewählten Visio-Formen exportiert wird.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ConvertVisioWithSelectiveShapes.py" >}}