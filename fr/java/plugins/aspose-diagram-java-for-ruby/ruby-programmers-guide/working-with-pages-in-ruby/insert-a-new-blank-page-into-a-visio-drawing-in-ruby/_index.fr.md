---
title: Insérer une nouvelle page vierge dans un dessin Visio en Ruby
type: docs
weight: 20
url: /fr/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Insérer une nouvelle page vierge dans un dessin Visio**
 Pour insérer une nouvelle page vierge dans un dessin Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**Ajouter une page** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def initialiser()

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

 Appelez le constructeur diagram pour charger diagram à partir d'un fichier VSD

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

 # Obtenir l'ID de page maximum

 maximum_page_identifiant = obtenir_maximum_page_id(diagram)

 # Initialiser un nouvel objet de page

 new_page = Rjb::import('com.aspose.diagram.Page').new

 # Définir le nom

 nouvelle_page.setName("nouvelle page")



 # Définir l'identifiant de la page

 Nouveau_page.setID(max_id_page + 1)

 # Ou essayez le constructeur Page

 # Page nouvellePage = nouvelle Page(MaxPageId + 1);

 # Ajouter une nouvelle page vierge

 diagram.getPages().add(nouvelle_page)

 # Enregistrer diagram

 diagram.save(données_dir + "NouvellePage_Sortie.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

 met "Ajout d'une nouvelle page."

fin

définitivement obtenir_maximum_page_id(diagram)

max = diagram.getPages().getPage(0).getID()

 je = 1

 alors que je< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Insérer une nouvelle page vierge dans un dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
