---
title: Exporter Visio Diagram vers XML en Ruby
type: docs
weight: 70
url: /fr/java/export-visio-diagram-to-xml-in-ruby/
---
## **Aspose.Diagram - Exportation VSD vers VDX**
Pour exporter VSD vers VDX en utilisant**Aspose.Diagram Java pour rubis** , appel**export_to_vdx** méthode de**Exporter versXml** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def export_to_vdx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VDX

    diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

    puts "Exported visio diagram to VDX."

end

{{< /highlight >}}
## **Aspose.Diagram - Exportation VSD vers VSX**
Pour exporter VSD vers VSX en utilisant**Aspose.Diagram Java pour rubis** , appel**export_to_vsx** méthode de**Exporter versXml** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def export_to_vsx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VSX

    diagram.save(data_dir + "Diagram.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)

    puts "Exported visio diagram to VSX."

end

{{< /highlight >}}
## **Aspose.Diagram - Exportation VSD vers VTX**
Pour exporter VSD vers VTX en utilisant**Aspose.Diagram Java pour rubis** , appel**export_to_vtx** méthode de**Exporter versXml** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 def export_to_vtx()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Save as VTX

    diagram.save(data_dir + "Diagram.vtx", Rjb::import('com.aspose.diagram.SaveFileFormat').VTX)

    puts "Exported visio diagram to VTX."

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers XML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxml.rb)
