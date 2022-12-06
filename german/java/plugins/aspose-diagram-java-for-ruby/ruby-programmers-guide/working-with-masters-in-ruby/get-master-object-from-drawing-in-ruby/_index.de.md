---
title: Holen Sie sich Master-Objekt vom Zeichnen in Ruby
type: docs
weight: 20
url: /de/java/get-master-object-from-drawing-in-ruby/
---
## **Aspose.Diagram – Abrufen eines Master-Objekts nach ID**
 So erhalten Sie ein Master-Objekt nach ID mit**Aspose.Diagram Java für Rubin** , Anruf**get_master_object_by_id** Methode von**GetMasterObject** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Aspose.Diagram – Abrufen eines Master-Objekts nach Name**
 So erhalten Sie ein Master-Objekt anhand des Namens mit**Aspose.Diagram Java für Rubin** , Anruf**get_master_object_by_name** Methode von**GetMasterObject** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**Master-Objekt aus Zeichnung abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
