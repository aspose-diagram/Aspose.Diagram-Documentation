---
title: Drucken von Diagram in VSTO und Aspose.Diagram
type: docs
weight: 100
url: /de/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
Unten ist der Code, um zu zeigen, wie man diagram druckt:

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 Druck der diagram an die**Standard Drucker** ist ganz einfach in Aspose.Diagram for .NET. Führen Sie die folgenden Schritte aus, um die diagram auf dem Standarddrucker zu drucken:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden, die gedruckt werden soll
- Rufen Sie die Print-Methode ohne Parameter auf, wie sie vom Diagram-Objekt verfügbar gemacht wird

 Druck der diagram an die**bestimmten Drucker** benötigt den Namen des Druckers als Parameter für die Print-Methode der Diagram. Führen Sie die folgenden Schritte aus, um die diagram auf dem gewünschten Drucker zu drucken:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden, die gedruckt werden soll
- Rufen Sie die Print-Methode der Klasse Diagram mit dem Druckernamen als Zeichenfolgenparameter für die Print-Methode auf

Unten ist der Code für die Verwendung des Standard- und spezifischen Druckers:

{{< highlight "cs" >}}

  string FilePath = "demo.vsd";

 //Load the diagram

 Diagram diagram = new Diagram(FilePath);

 //Call the print method to print whole Diagram to the default printer

 diagram.Print();

 //Call the print method to print whole Diagram to the desired printer

 diagram.Print("LaserJet1100");

 PrinterSettings settings = new PrinterSettings();

 settings.PrinterName = "LaserJet1100";

 //Call the print method to print whole Diagram to the desired printer and set document name in print job

 diagram.Print(settings, "Job name while printing with Aspose.Diagram");


{{< /highlight >}}
## **Beispielcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Laufcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
