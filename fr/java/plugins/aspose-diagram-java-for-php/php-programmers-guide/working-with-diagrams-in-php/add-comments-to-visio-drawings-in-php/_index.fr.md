---
title: Ajouter des commentaires aux dessins Visio en PHP
type: docs
weight: 10
url: /fr/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - Ajouter des commentaires aux dessins Visio**
 Pour ajouter des commentaires aux dessins Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**AjouterCommentaireAuDiagramme** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Add comment

$diagram->getPages()->getPage(0)->addComment(7.205905511811023, 3.880708661417323, "test@");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddComment.vdx", $saveFileFormat->VDX);

print "Added comment successfully!".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Ajouter des commentaires aux dessins Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
