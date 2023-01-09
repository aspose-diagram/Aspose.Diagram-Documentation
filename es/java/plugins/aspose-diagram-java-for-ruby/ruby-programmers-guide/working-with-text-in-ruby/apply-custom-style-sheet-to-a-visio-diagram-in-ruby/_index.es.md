---
title: Aplique una hoja de estilo personalizada a un Visio Diagram en Ruby
type: docs
weight: 10
url: /es/java/apply-custom-style-sheet-to-a-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Aplicar hoja de estilo personalizado a un Visio Diagram**
 Para aplicar una hoja de estilo personalizada a un Visio Diagram usando**Aspose.Diagram Java para rubí** , simplemente invocar**ApplyCustomStyleSheet** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

formas = diagram.getPages().getPage(0).getShapes()

yo = 0

 mientras yo< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        source_shape = shape

        break

    end

    i +=1

end

\# Find the required style sheet

stylesheets = diagram.getStyleSheets()

j = 0

while j < stylesheets.getCount()

    stylesheet = stylesheets.get(j)

    if stylesheet.getName() == "Basic"

        custom_stylesheet = stylesheet

        break

    end

    j +=1

end

if source_shape != nil && custom_stylesheet != nil

    # Apply text style

    source_shape.setTextStyle(custom_stylesheet)

    # Apply fill style

    source_shape.setFillStyle(custom_stylesheet)

    # Apply line style

    source_shape.setLineStyle(custom_stylesheet)

end

\# Save diagram

diagram.save(data_dir + "ApplyCustomStyleSheet.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied custom stylesheet to a visio diagram."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Aplicar hoja de estilo personalizado a un Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/applycustomstylesheet.rb)
