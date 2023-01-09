---
title: Imprimiendo un Diagram en VSTO y Aspose.Diagram
type: docs
weight: 100
url: /es/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
A continuación se muestra el código para mostrar cómo imprimir diagram:

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 Impresión del diagram al**impresora predeterminada** es bastante simple en Aspose.Diagram for .NET. Realice los siguientes pasos para imprimir el diagram en la impresora predeterminada:

- Cree una instancia de la clase Diagram para cargar un diagram que se imprimirá
- Llame al método de impresión sin parámetros expuestos por el objeto Diagram

 Impresión del diagram al**impresora específica** requiere el nombre de la impresora como parámetro para el método de impresión del Diagram. Realice los siguientes pasos para imprimir el diagram en la impresora deseada:

- Cree una instancia de la clase Diagram para cargar un diagram que se imprimirá
- Llame al método de impresión de la clase Diagram con el nombre de la impresora como parámetro de cadena para el método de impresión

A continuación se muestra el código de uso de la impresora predeterminada y específica:

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
## **Descargar código de muestra**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Descargar código de ejecución**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
