---
title: Skriver ut en Diagram i VSTO och Aspose.Diagram
type: docs
weight: 100
url: /sv/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
Nedan finns koden för att visa hur man skriver ut diagram:

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 Utskrift av diagram till**standardskrivare** är ganska enkelt i Aspose.Diagram for .NET. Utför följande steg för att skriva ut diagram till standardskrivaren:

- Skapa en instans av klassen Diagram för att ladda en diagram som ska skrivas ut
- Anropa utskriftsmetoden utan parametrar som exponeras av objektet Diagram

 Utskrift av diagram till**specifik skrivare** kräver skrivarens namn som parameter för utskriftsmetoden för Diagram. Utför följande steg för att skriva ut diagram till önskad skrivare:

- Skapa en instans av klassen Diagram för att ladda en diagram som ska skrivas ut
- Anropa utskriftsmetoden för klassen Diagram med skrivarnamn som strängparameter till utskriftsmetoden

Nedan är koden för att använda standardskrivare och specifik skrivare:

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
## **Ladda ner exempelkod**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Ladda ner Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
