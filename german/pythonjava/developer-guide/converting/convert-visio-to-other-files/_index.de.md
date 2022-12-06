---
title:  Konvertieren Sie Visio in andere Formate
linktitle:  Konvertieren Sie Visio in andere Formate
type: docs
weight: 40
url: /de/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML ,XAML mit ein paar Zeilen Code.
---
**[A Microsoft Visio diagram soll exportiert werden.](ExportToXML.vsd)**

## **Exportieren nach XML**
In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in XML exportieren, indem Sie Aspose.Diagram für Python über Java verwenden.

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

## **Export nach XPS**
In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram nach XPS exportieren, indem Sie Aspose.Diagram für Python über Java verwenden.
Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

Die Codeausschnitte in diesem Artikel verwenden die folgende diagram als Eingabe. Sie können auch andere diagram-Formate (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX oder VSX) verwenden.

So exportieren Sie VSD diagram nach XPS:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse Diagram auf und legen Sie XPS als Ausgabeformat fest.

Das folgende Bild zeigt die XPS-Ausgabedatei.

### **Exportieren nach XPS Programmierbeispiel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **Exportieren einer Diagram in SVG**
In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in SVG (Scalable Vector Graphics) exportieren, indem Sie Aspose.Diagram für Python über Java verwenden.

Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

Führen Sie die folgenden Schritte aus, um VSD diagram in SVG zu exportieren:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse auf und legen Sie SVG als Exportformat fest.

### **Exportieren von Diagram in das SVG-Programmierbeispiel**
Die Codebeispiele zeigen, wie ein diagram mithilfe von Java in SVG exportiert wird.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **Exportieren einer Diagram in XAML**
In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram in XAML (Extensible Application Markup Language) exportieren, indem Sie Aspose.Diagram für Python über Java verwenden.

Verwenden Sie den Konstruktor der Diagram-Klasse, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

So exportieren Sie eine VSD diagram in XAML:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse auf und legen Sie XAML als Exportformat fest.

### **Exportieren in das XAML-Programmierbeispiel**
Das Codebeispiel zeigt, wie ein diagram mithilfe von Java in XAML exportiert wird.

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