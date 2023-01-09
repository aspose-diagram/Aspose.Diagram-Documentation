---
title: Ajouter des commentaires à Visio Dessins en rubis
type: docs
weight: 40
url: /fr/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - Ajouter des commentaires aux dessins Visio**
 Pour ajouter des commentaires aux dessins Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**AjouterCommentaireAuDiagramme** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add comment

diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

\# Save as VDX

diagram.save(data_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added comment successfully!"

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Ajouter des commentaires aux dessins Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
