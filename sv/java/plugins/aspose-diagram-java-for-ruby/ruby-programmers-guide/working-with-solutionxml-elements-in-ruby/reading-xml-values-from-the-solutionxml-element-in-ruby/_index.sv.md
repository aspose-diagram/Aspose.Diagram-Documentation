---
title: Läser XML-värden från SolutionXML-elementet i Ruby
type: docs
weight: 20
url: /sv/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram - Läsa XML-värden från SolutionXML-elementet**
 För att läsa XML-värden från SolutionXML-elementet med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**ReadXmlValues** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FIL__)))) + '/data/'

\# Skapa instans av Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs()

i = 0

 medan jag< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Läsa XML-värden från SolutionXML Element (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
