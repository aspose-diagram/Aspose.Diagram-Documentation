---
title: Agregar Comentarios a Visio Dibujos en Ruby
type: docs
weight: 40
url: /es/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - Agregar comentarios a Visio Dibujos**
 Para agregar comentarios a Visio Dibujos usando**Aspose.Diagram Java para rubí** , simplemente invocar**AgregarComentarioAlDiagrama** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add comment

diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

\# Save as VDX

diagram.save(data_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added comment successfully!"

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Agregar Comentarios a Visio Dibujos (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
