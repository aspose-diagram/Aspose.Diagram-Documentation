---
title: Läsa XML-värden från SolutionXML-elementet i PHP
type: docs
weight: 20
url: /sv/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram - Läsa XML-värden från SolutionXML-elementet**
 För att läsa XML-värden från SolutionXML-elementet med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ReadXmlValues** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Läsa XML-värden från SolutionXML Element (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
