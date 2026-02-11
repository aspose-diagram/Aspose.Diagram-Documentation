---
title: Trabajando con Imprimir
type: docs
weight: 80
url: /es/java/working-with-print/
---
## **Imprimiendo un Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) proporciona cuatro métodos de sobrecarga para la impresión de los diagramas. Estos métodos son lo suficientemente flexibles para imprimir el diagram en la impresora predeterminada o en cualquiera de las impresoras disponibles con configuraciones personalizadas. Solo necesita seleccionar el método de impresión apropiado de acuerdo con el requisito.
### **Impresión en una impresora específica**
La impresión del diagram en la impresora específica requiere el nombre de la impresora como parámetro para el método de impresión del Diagram. Realice los siguientes pasos para imprimir el diagram en la impresora deseada:

- Cree una instancia de la clase Diagram para cargar un diagram que se imprimirá
- Llame al método de impresión de la clase Diagram con el nombre de la impresora como parámetro de cadena para el método de impresión
#### **Muestra de programación de impresión en una impresora específica**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}

### **Configuración del nombre de la impresora y del documento**
Aspose.Diagram Las API permiten configurar la impresora específica y el nombre del documento para un trabajo de impresión. Realice los siguientes pasos para imprimir el diagram en la impresora deseada:

- Cree una instancia de la clase Diagram para cargar un diagram que se imprimirá
- Llame al método de impresión de la clase Diagram con la impresora y el nombre del documento como parámetro de cadena para el método de impresión
#### **Configuración de la impresora y el nombre del documento Ejemplo de programación**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

