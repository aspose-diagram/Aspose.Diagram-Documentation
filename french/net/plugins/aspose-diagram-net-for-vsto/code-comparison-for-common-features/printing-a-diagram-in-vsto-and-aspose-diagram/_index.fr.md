---
title: Impression d'un Diagram en VSTO et Aspose.Diagram
type: docs
weight: 100
url: /fr/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
Ci-dessous le code pour montrer comment imprimer diagram :

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 Impression du diagram au**imprimante par défaut** est assez simple en Aspose.Diagram for .NET. Effectuez les étapes suivantes pour imprimer le diagram sur l'imprimante par défaut :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print sans paramètres comme exposé par l'objet Diagram

 Impression du diagram au**imprimante spécifique** nécessite le nom de l'imprimante comme paramètre de la méthode d'impression du Diagram. Effectuez les étapes suivantes pour imprimer le diagram sur l'imprimante souhaitée :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print de la classe Diagram avec le nom de l'imprimante comme paramètre de chaîne à la méthode Print

Vous trouverez ci-dessous le code d'utilisation de l'imprimante par défaut et spécifique :

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
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Télécharger le code d'exécution**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
