---
title: Rédaction du résumé du document
type: docs
weight: 70
url: /fr/net/writing-document-summary/
---
## **VSTO**
Vous trouverez ci-dessous le code d'écriture du résumé du document Visio :

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio vous permet de définir un certain nombre de propriétés d'informations de résumé de document pour vous aider, vous et vos collègues, à identifier un diagram. Les propriétés de résumé, par exemple le titre, le sujet, l'auteur et la description, rendent le fichier plus facile à trouver lors de la recherche et plus facile à reconnaître lors de la navigation des dossiers.

{{% /alert %}} 
### **Rédaction Microsoft Visio Résumé du document Info**
 La[Propriétés du document](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)La classe expose un certain nombre de propriétés pour définir ou obtenir les informations récapitulatives d'un Microsoft Visio diagram. Aspose.Diagram for .NET peut mettre à jour les informations récapitulatives du dessin, puis réécrire le fichier de dessin dans VDX.

Pour mettre à jour les informations récapitulatives du dessin d'un fichier VDX ou VSD existant :

1.  Créer une instance de[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) classer.
1. Définissez les propriétés exposées par Diagram.DocumentProps pour définir les informations récapitulatives du fichier de dessin Visio.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VDX.

Vérifiez les informations récapitulatives :

1. Ouvrez le fichier de sortie VDX dans Microsoft Visio.
1.  Sélection**Info** du**Dossier** menu.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Télécharger le code d'exécution**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
