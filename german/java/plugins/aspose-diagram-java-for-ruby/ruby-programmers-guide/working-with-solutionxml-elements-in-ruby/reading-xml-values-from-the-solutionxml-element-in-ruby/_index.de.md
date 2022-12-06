---
title: Lesen von XML-Werten aus dem SolutionXML-Element in Ruby
type: docs
weight: 20
url: /de/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram – Lesen von XML-Werten aus dem SolutionXML-Element**
 So lesen Sie XML-Werte aus dem SolutionXML-Element mit**Aspose.Diagram Java für Rubin** , einfach aufrufen**ReadXmlValues** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

{{< highlight "ruby" >}}

 Daten_dir = Datei.dirname(Datei.dirname(Datei.dirname(Datei.dirname(__DATEI__)))) + '/data/'

\# Instanz von Diagram erstellen

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs()

ich = 0

 während ich< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Lesen von XML-Werten aus dem SolutionXML-Element (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
