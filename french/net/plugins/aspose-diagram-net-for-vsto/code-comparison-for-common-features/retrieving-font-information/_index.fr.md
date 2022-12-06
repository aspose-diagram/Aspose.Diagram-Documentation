---
title: Récupération des informations sur la police
type: docs
weight: 80
url: /fr/net/retrieving-font-information/
---
## **VSTO**
Vous trouverez ci-dessous le code permettant de récupérer les informations sur la police :

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram a des mécanismes pour récupérer des informations sur les éléments qui composent un diagram, à partir de[pages](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) , pochoirs,[connecteurs](/diagram/fr/net/retrieving-connector-information/)et aussi les polices. Cet article montre comment savoir quelles polices sont utilisées dans un diagram.

{{% /alert %}} 

 La[Police de caractère](https://reference.aspose.com/diagram/net/aspose.diagram/font) L'objet représente une police de caractères qui est soit appliquée au texte d'un document, soit disponible pour une utilisation sur le système.

Un objet Font mappe un nom (par exemple, « Arial ») à l'ID de police (par exemple, 3) que Microsoft Visio stocke dans une cellule Police d'une section Caractère d'une forme qui contient du texte mis en forme avec cette police. Les ID de police peuvent changer lorsqu'un document est ouvert sur différents systèmes ou lorsque des polices sont installées ou supprimées.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Télécharger le code d'exécution**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
