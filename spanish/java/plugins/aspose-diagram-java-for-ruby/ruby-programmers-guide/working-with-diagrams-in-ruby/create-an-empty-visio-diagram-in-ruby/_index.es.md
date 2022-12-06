---
title: Cree un Visio Diagram vacío en Ruby
type: docs
weight: 10
url: /es/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Crear un vacío Visio Diagram**
 Para crear un Visio Diagram vacío usando**Aspose.Diagram Java para rubí** , simplemente invocar**CrearDiagrama** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Cree un Visio Diagram (Aspose.Diagram) vacío**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
