---
title: Recupero delle informazioni sul connettore
type: docs
weight: 90
url: /it/net/retrieving-connector-information/
---
## **VSTO**
Di seguito è riportato il codice per ottenere informazioni sul connettore:

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram for .NET fornisce meccanismi per il recupero di informazioni - ID e nome - su[pagine](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) e[maestro](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). Consente inoltre di ottenere informazioni sui connettori, gli elementi che collegano le forme.

{{% /alert %}} 

 Il[Collegare](https://reference.aspose.com/diagram/net/aspose.diagram/connect) oggetto rappresenta un connettore che unisce due forme in una pagina di disegno Visio. La proprietà Connects, esposta da[Pagina](https://reference.aspose.com/diagram/net/aspose.diagram/page) class supporta una raccolta di oggetti Aspose.Diagram.Connect. Questa proprietà può essere utilizzata per recuperare informazioni su ID e nome su un connettore.

Di seguito è riportato il codice per ottenere informazioni sul connettore utilizzando Aspose.Diagram .NET:

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
## **Scarica il codice di esempio**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Scarica il codice in esecuzione**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
