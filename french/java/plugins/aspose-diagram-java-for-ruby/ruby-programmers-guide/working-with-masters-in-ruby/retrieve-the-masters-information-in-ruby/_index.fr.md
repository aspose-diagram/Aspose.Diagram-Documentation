---
title: Récupérer les informations de Master en Ruby
type: docs
weight: 30
url: /fr/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - Récupérer les informations du Master**
 Pour récupérer les informations sur les masters à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**GetMasterInfo** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Appelez le constructeur diagram pour charger diagram à partir d'un fichier VSD

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

maîtres = diagram.getMasters()

je = 0

 alors que je< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations sur les maîtres (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
