---
title: Lecture des valeurs XML à partir de l'élément SolutionXML dans Ruby
type: docs
weight: 20
url: /fr/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram - Lecture des valeurs XML à partir de l'élément SolutionXML**
 Pour lire des valeurs XML à partir de l'élément SolutionXML à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**LireValeursXml** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs()

je = 0

 alors que je< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Lecture des valeurs XML à partir de l'élément SolutionXML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
