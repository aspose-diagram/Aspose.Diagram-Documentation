---
title: Recupera le informazioni sulla forma Visio in Ruby
type: docs
weight: 70
url: /it/java/retrieve-visio-shape-information-in-ruby/
---
## **Aspose.Diagram - Recupera Visio Informazioni sulla forma**
 Per recuperare Visio Informazioni sulla forma utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Ottieni InfoForma** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

forme = diagram.getPages().getPage(0).getShapes()

io = 0

 mentre io< shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera Visio Informazioni sulla forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
