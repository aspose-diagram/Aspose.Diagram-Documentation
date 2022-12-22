---
title: Lettura di valori XML dall'elemento SolutionXML in Ruby
type: docs
weight: 20
url: /it/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram - Lettura di valori XML dall'elemento SolutionXML**
 Per leggere i valori XML dall'elemento SolutionXML utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**ReadXmlValues** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

{{< highlight "ruby" >}}

 dati_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/dati/'

\# Crea un'istanza di Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

soluzione_xmls = diagram.getSolutionXMLs()

io = 0

 mentre io< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Lettura di valori XML dall'elemento SolutionXML (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
