---
title: Récupération des informations sur le connecteur
type: docs
weight: 90
url: /fr/net/retrieving-connector-information/
---
## **VSTO**
Voici le code pour obtenir des informations sur le connecteur :

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram for .NET fournit des mécanismes pour récupérer des informations - ID et nom - sur[pages](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) et[Maître](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). Il vous permet également d'obtenir des informations sur les connecteurs, les éléments qui relient les formes.

{{% /alert %}} 

 La[Relier](https://reference.aspose.com/diagram/net/aspose.diagram/connect) L'objet représente un connecteur qui relie deux formes sur une page de dessin Visio. La propriété Connects, exposée par la[Page](https://reference.aspose.com/diagram/net/aspose.diagram/page) prend en charge une collection d'objets Aspose.Diagram.Connect. Cette propriété peut être utilisée pour récupérer des informations d'ID et de nom sur un connecteur.

Vous trouverez ci-dessous le code permettant d'obtenir des informations sur le connecteur en utilisant Aspose.Diagram .NET :

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
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Télécharger le code d'exécution**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
