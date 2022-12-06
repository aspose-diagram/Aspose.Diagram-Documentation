---
title: Récupérer les informations des connecteurs Visio dans Ruby
type: docs
weight: 20
url: /fr/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - Récupérer les informations sur les connecteurs Visio**
 Pour récupérer les informations sur les connecteurs Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**GetConnectorsInfo** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

connecteurs = diagram.getPages().getPage(0).getConnects()

je = 0

 alors que je< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations sur les connecteurs Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

