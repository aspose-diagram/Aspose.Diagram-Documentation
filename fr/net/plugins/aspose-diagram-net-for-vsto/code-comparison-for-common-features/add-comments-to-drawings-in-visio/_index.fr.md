---
title: Ajouter des commentaires aux dessins dans Visio
type: docs
weight: 40
url: /fr/net/add-comments-to-drawings-in-visio/
---
## **VSTO**
Ci-dessous le code pour ajouter des commentaires au diagram :

{{< highlight "cs" >}}

  Page mypage= Application.ActiveDocument.Pages[1];

 mypage.Comments.Add("Test");

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET vous permet de placer des commentaires n'importe où sur une page diagram.

{{% /alert %}} 

La méthode AddComment, exposée par la classe Page, vous permet d'ajouter des commentaires à une page de dessin. Il prend les coordonnées X et Y avec une chaîne de commentaire. Voici l'extrait de code :

{{< highlight "cs" >}}

  // Load diagram

 Diagram diagram = new Diagram("Drawing1.vsd");

 // Add comment

 diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

 // Save diagram

 diagram.Save("Output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Télécharger le code d'exécution**
- [GithubGenericName](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Add%20Comment)
