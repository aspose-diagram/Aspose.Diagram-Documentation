---
title: Arbeiten mit Drucken
type: docs
weight: 80
url: /de/java/working-with-print/
---
## **Drucken einer Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) bietet vier Überladungsmethoden zum Drucken der Diagramme. Diese Methoden sind flexibel genug, um die diagram auf dem Standarddrucker oder auf einem der verfügbaren Drucker mit benutzerdefinierten Einstellungen zu drucken. Sie müssen lediglich je nach Anforderung das passende Druckverfahren auswählen.
### **Drucken auf einem bestimmten Drucker**
Das Drucken von diagram auf dem spezifischen Drucker erfordert den Namen des Druckers als Parameter für die Print-Methode von Diagram. Führen Sie die folgenden Schritte aus, um diagram auf dem gewünschten Drucker zu drucken:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden, die gedruckt werden soll
- Rufen Sie die Print-Methode der Klasse Diagram mit dem Druckernamen als Zeichenfolgenparameter für die Print-Methode auf
#### **Drucken auf einem bestimmten Drucker Programmierbeispiel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}

### **Einstellen von Drucker und Dokumentname**
Aspose.Diagram APIs ermöglicht das Festlegen des spezifischen Drucker- und Dokumentnamens für einen Druckauftrag. Führen Sie die folgenden Schritte aus, um die diagram auf dem gewünschten Drucker auszudrucken:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden, die gedruckt werden soll
- Rufen Sie die Print-Methode der Klasse Diagram mit dem Drucker- und Dokumentnamen als Zeichenfolgenparameter für die Print-Methode auf
#### **Beispiel für die Programmierung des Druckers und des Dokumentnamens**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

