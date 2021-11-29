---
title: Retrieving Connector Information
type: docs
weight: 90
url: /net/retrieving-connector-information/
---

## **VSTO**
Below is the code to get connector information:

{{< highlight cs >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET provides mechanisms for retrieving information - ID and name - about [pages](/pages/createpage.action?spaceKey=diagramnet&title=Retrieving+Page+Information&linkCreation=true&fromPageId=18354905) and [master](/pages/createpage.action?spaceKey=diagramnet&title=Retrieving+Master+Information&linkCreation=true&fromPageId=18354905). It also lets you get information about connectors, the elements that link shapes.

{{% /alert %}} 

The [Connect](/pages/createpage.action?spaceKey=diagramnet&title=Connect+Class&linkCreation=true&fromPageId=18354905) object represents a connector that joins two shapes on a Visio drawing page. The Connects property, exposed by the [Page](/pages/createpage.action?spaceKey=diagramnet&title=Page+Class&linkCreation=true&fromPageId=18354905) class supports a collection of Aspose.Diagram.Connect objects. This property can be used to retrieve ID and name information about a connector.

Below is the code to get connector information using Aspose.Diagram .NET:

{{< highlight cs >}}

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
## **Download Sample Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Download Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
