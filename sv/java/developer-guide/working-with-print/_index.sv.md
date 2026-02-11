---
title: Arbeta med Print
type: docs
weight: 80
url: /sv/java/working-with-print/
---
## **Skriver ut en Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) tillhandahåller fyra överbelastningsmetoder för utskrift av diagrammen. Dessa metoder är tillräckligt flexibla för att skriva ut diagram till standardskrivaren eller till någon av de tillgängliga skrivarna med anpassade inställningar. Du behöver bara välja lämplig utskriftsmetod enligt kraven.
### **Utskrift till specifik skrivare**
Utskrift av diagram till den specifika skrivaren kräver skrivarens namn som parameter för utskriftsmetoden för Diagram. Utför följande steg för att skriva ut diagram till önskad skrivare:

- Skapa en instans av klassen Diagram för att ladda en diagram som ska skrivas ut
- Anropa utskriftsmetoden för klassen Diagram med skrivarnamn som strängparameter till utskriftsmetoden
#### **Utskrift till specifik skrivarprogrammeringsexempel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}

### **Ställa in skrivare och dokumentnamn**
Aspose.Diagram API:er gör det möjligt att ställa in det specifika skrivar- och dokumentnamnet för ett utskriftsjobb. Utför följande steg för att skriva ut diagram till önskad skrivare:

- Skapa en instans av klassen Diagram för att ladda en diagram som ska skrivas ut
- Anropa utskriftsmetoden för klassen Diagram med skrivare och dokumentnamn som strängparameter till utskriftsmetoden
#### **Inställning av skrivare och dokumentnamn Programmeringsexempel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

