---
title: Lavorare con Stampa
type: docs
weight: 80
url: /it/java/working-with-print/
---
## **Stampa un Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) fornisce quattro metodi di overload per la stampa dei diagrammi. Questi metodi sono sufficientemente flessibili per stampare lo diagram sulla stampante predefinita o su qualsiasi stampante disponibile con impostazioni personalizzate. Devi solo selezionare il metodo di stampa appropriato in base al requisito.
### **Stampa su stampante specifica**
La stampa dello diagram sulla stampante specifica richiede il nome della stampante come parametro per il metodo di stampa dello Diagram. Effettuare le seguenti operazioni per stampare lo diagram sulla stampante desiderata:

- Crea un'istanza della classe Diagram per caricare un diagram che deve essere stampato
- Chiamare il metodo Print della classe Diagram con il nome della stampante come parametro di stringa al metodo Print
#### **Esempio di programmazione della stampa su una stampante specifica**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}

### **Impostazione della stampante e del nome del documento**
Aspose.Diagram API consente di impostare la stampante specifica e il nome del documento per un lavoro di stampa. Effettuare le seguenti operazioni per stampare lo diagram sulla stampante desiderata:

- Crea un'istanza della classe Diagram per caricare un diagram che deve essere stampato
- Chiamare il metodo Print della classe Diagram con la stampante e il nome del documento come parametro di stringa al metodo Print
#### **Impostazione della stampante e del nome del documento Esempio di programmazione**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

