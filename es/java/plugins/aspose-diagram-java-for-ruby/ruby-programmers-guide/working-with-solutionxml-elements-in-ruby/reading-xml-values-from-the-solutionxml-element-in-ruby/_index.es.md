---
title: Lectura de valores XML del elemento SolutionXML en Ruby
type: docs
weight: 20
url: /es/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram - Lectura de valores XML del elemento SolutionXML**
 Para leer valores XML del elemento SolutionXML usando**Aspose.Diagram Java para rubí** , simplemente invocar**Leer valores Xml** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 datos_dir = Archivo.dirname(Archivo.dirname(Archivo.dirname(Archivo.dirname(__EXPEDIENTE__)))) + '/datos/'

\# Crear instancia de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs()

yo = 0

 mientras yo< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Lectura de valores XML del elemento SolutionXML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
