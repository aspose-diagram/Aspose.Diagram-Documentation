---
title: Abrufen von Connector-Informationen
type: docs
weight: 90
url: /de/net/retrieving-connector-information/
---
## **VSTO**
Unten ist der Code zum Abrufen von Connector-Informationen:

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram for .NET bietet Mechanismen zum Abrufen von Informationen – ID und Name – über[Seiten](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) und[Meister](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). Außerdem erhalten Sie Informationen zu Verbindungselementen, den Elementen, die Formen verbinden.

{{% /alert %}} 

 Das[Verbinden](https://reference.aspose.com/diagram/net/aspose.diagram/connect) -Objekt stellt einen Verbinder dar, der zwei Shapes auf einem Zeichenblatt Visio verbindet. Die Connects-Eigenschaft, verfügbar gemacht durch die[Buchseite](https://reference.aspose.com/diagram/net/aspose.diagram/page) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Connect-Objekten. Diese Eigenschaft kann verwendet werden, um ID- und Namensinformationen zu einem Connector abzurufen.

Unten ist der Code zum Abrufen von Connector-Informationen mit Aspose.Diagram .NET:

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
## **Beispielcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Laufcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
