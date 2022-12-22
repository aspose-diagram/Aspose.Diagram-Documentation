---
title: Obtenir l'objet principal du dessin dans Ruby
type: docs
weight: 20
url: /fr/java/get-master-object-from-drawing-in-ruby/
---
## **Aspose.Diagram - Obtention d'un objet principal par ID**
 Pour obtenir un objet principal par ID à l'aide de**Aspose.Diagram Java pour rubis** , appel**get_master_object_by_id** méthode de**GetMasterObject** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def get_master_object_by_id()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    master_id = 2

    # Get master object by id

    master = diagram.getMasters().getMaster(master_id)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

end

{{< /highlight >}}
## **Aspose.Diagram - Obtention d'un objet principal par nom**
 Pour obtenir un objet principal par nom à l'aide**Aspose.Diagram Java pour rubis** , appel**get_master_object_by_name** méthode de**GetMasterObject** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def get_master_object_by_name()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set master name

    master_name = "Background tranquil .2"

    # Get master object by name

    master = diagram.getMasters().getMasterByName(master_name)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Obtenir l'objet principal du dessin (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
