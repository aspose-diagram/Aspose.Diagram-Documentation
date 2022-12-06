---
title: Compruebe la presencia de un maestro en el dibujo Visio en Ruby
type: docs
weight: 10
url: /es/java/check-presence-of-a-master-in-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Comprobación de la presencia de un maestro por ID**
 Para verificar la presencia de un maestro por ID usando**Aspose.Diagram Java para rubí** , llamar**check_presence_master_by_id** método de**comprobar la presencia del maestro** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def check_presence_master_by_id()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    master_id = 2

    # check master by id

    is_present = diagram.getMasters().isExist(master_id)

    puts "Master Presence : " + is_present.to_s

end

{{< /highlight >}}
## **Aspose.Diagram - Comprobación de la presencia de un maestro por nombre**
 Para verificar la presencia de un maestro por nombre usando**Aspose.Diagram Java para rubí** , llamar**check_presence_master_by_name** método de**comprobar la presencia del maestro** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 def check_presence_master_by_name()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set master name

    master_name = "Background tranquil .2"

    # check master object by name

    is_present = diagram.getMasters().isExist(master_name)

    puts "Master Presence : " + is_present.to_s

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Compruebe la presencia de un maestro en el dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/checkpresenceofmaster.rb)
