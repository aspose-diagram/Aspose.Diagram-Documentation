---
title: Working with Print
type: docs
weight: 80
url: /java/working-with-print/
---

## **Printing a Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) provides four overloads methods for printing of the diagrams. These methods are flexible enough to print the diagram to the default printer or to any of the available printer with customized settings. You only need to select the appropriate print method according to the requirement.
### **Printing to specific printer**
Printing of the diagram to the specific printer requires the name of the printer as parameter to the Print method of the Diagram. Perform the following steps in order to print the diagram to the desired printer:

- Create an instance of Diagram class to load a diagram that is to be printed
- Call the Print method of the Diagram class with printer name as string parameter to the Print method
#### **Printing to Specific Printer Programming Sample**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}
```
### **Setting Printer and Document Name**
Aspose.Diagram APIs allows to set the specific printer and document name for a print job. Perform the following steps in order to print the diagram to the desired printer:

- Create an instance of Diagram class to load a diagram that is to be printed
- Call the Print method of the Diagram class with printer and document name as string parameter to the Print method
#### **Setting Printer and Document Name Programming Sample**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}
```
