---
title: Recuperar información de fuentes de dibujo en Ruby
type: docs
weight: 30
url: /es/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - Recuperar información de fuente de dibujo**
 Para recuperar información de fuentes de dibujo usando**Aspose.Diagram Java para rubí** , simplemente invocar**ObtenerDiagramFontInfo** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').nuevo(data_dir + "Dibujo.vsd")

fuentes = diagram.getFonts()

yo = 0

 mientras yo< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar información de fuente de dibujo (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
