---
title: Lecture des valeurs XML à partir de l'élément SolutionXML en PHP
type: docs
weight: 20
url: /fr/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram - Lecture des valeurs XML à partir de l'élément SolutionXML**
 Pour lire des valeurs XML à partir de l'élément SolutionXML à l'aide**Aspose.Diagram Java pour PHP** , invoquez simplement**LireValeursXml** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vdx");

$solution_xmls=$diagram->getSolutionXMLs();

$i= 0;

while ($i<(int)(string)$solution_xmls->getCount()) {

$solution_xml =$solution_xmls->get($i);

\# get name property

print "Name: ".(string)$solution_xml->getName();

\# get xml value

print "Value:".(string)$solution_xml->getXmlValue();

$i += 1;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Lecture des valeurs XML à partir de l'élément SolutionXML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
