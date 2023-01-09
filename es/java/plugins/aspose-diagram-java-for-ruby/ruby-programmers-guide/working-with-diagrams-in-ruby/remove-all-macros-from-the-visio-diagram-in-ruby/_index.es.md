---
title: Eliminar todas las macros del Visio Diagram en Ruby
type: docs
weight: 50
url: /es/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Eliminar todas las macros del Visio Diagram**
 Para quitar todas las macros del Visio Diagram usando**Aspose.Diagram Java para rubí** , simplemente invocar**Quitar todas las macros del diagrama** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

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
## **Descargar código de ejecución**
 Descargar**Eliminar todas las macros del Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
