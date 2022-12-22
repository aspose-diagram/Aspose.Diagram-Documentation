---
title: Stampa di un Diagram in VSTO e Aspose.Diagram
type: docs
weight: 100
url: /it/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
Di seguito il codice per mostrare come stampare diagram:

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 Stampa dello diagram al**stampante predefinita** è abbastanza semplice in Aspose.Diagram for .NET. Eseguire i seguenti passaggi per stampare diagram sulla stampante predefinita:

- Crea un'istanza della classe Diagram per caricare un diagram che deve essere stampato
- Chiamare il metodo Print senza parametri come esposto dall'oggetto Diagram

 Stampa dello diagram al**stampante specifica** richiede il nome della stampante come parametro al metodo Print dello Diagram. Eseguire i seguenti passaggi per stampare lo diagram sulla stampante desiderata:

- Crea un'istanza della classe Diagram per caricare un diagram che deve essere stampato
- Chiamare il metodo Print della classe Diagram con il nome della stampante come parametro di stringa al metodo Print

Di seguito è riportato il codice di utilizzo della stampante predefinita e specifica:

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
## **Scarica il codice di esempio**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Scarica il codice in esecuzione**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
