---
title: Supprimer toutes les macros du Visio Diagram dans Ruby
type: docs
weight: 50
url: /fr/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Supprimer toutes les macros du Visio Diagram**
 Pour supprimer toutes les macros du Visio Diagram à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**RemoveAllMacrosFromDiagram** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# remove all macros

diagram.setVbProjectData(nil)

\# Save as VDX

diagram.save(data_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Removed all macros from diagram successfully!"

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Supprimer toutes les macros du Visio Diagram (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
