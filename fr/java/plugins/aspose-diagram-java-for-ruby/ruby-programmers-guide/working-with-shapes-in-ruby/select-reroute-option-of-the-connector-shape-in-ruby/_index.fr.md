---
title: Sélectionnez l'option de réacheminement de la forme du connecteur dans Ruby
type: docs
weight: 90
url: /fr/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram - Sélectionnez l'option de réacheminement de la forme du connecteur**
 Pour sélectionner l'option de réacheminement de la forme du connecteur à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**SelectRerouteOption** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set reroute option

shape.getLayout().getConFixedCode().setValue(Rjb::import('com.aspose.diagram.ConFixedCodeValue').NEVER_REROUTE)

\# Save diagram

diagram.save(data_dir + "SelectRerouteOption.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Seleted reroute option of the connector shape."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Sélectionnez l'option de réacheminement de la forme du connecteur (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
