---
title: Hämtar anslutningsinformation
type: docs
weight: 90
url: /sv/net/retrieving-connector-information/
---
## **VSTO**
Nedan är koden för att få kontaktinformation:

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram for .NET tillhandahåller mekanismer för att hämta information - ID och namn - om[sidor](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) och[bemästra](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). Det låter dig också få information om kontakter, de element som länkar former.

{{% /alert %}} 

 De[Ansluta](https://reference.aspose.com/diagram/net/aspose.diagram/connect) objektet representerar en koppling som förenar två former på en Visio ritsida. Connects-egendomen, exponerad av[Sida](https://reference.aspose.com/diagram/net/aspose.diagram/page) klass stöder en samling av Aspose.Diagram. Connect-objekt. Den här egenskapen kan användas för att hämta ID- och namninformation om en koppling.

Nedan finns koden för att få kontaktinformation med Aspose.Diagram .NET:

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[1].Connects)

 {

   //Display information about the Connectors

   Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);

   Console.WriteLine("To Shape ID : " + connector.ToSheet);

 }

 Console.ReadLine();


{{< /highlight >}}
## **Ladda ner exempelkod**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Ladda ner Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
