---
title: Lesen von XML-Werten aus dem SolutionXML-Element in PHP
type: docs
weight: 20
url: /de/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram – Lesen von XML-Werten aus dem SolutionXML-Element**
 So lesen Sie XML-Werte aus dem SolutionXML-Element mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ReadXmlValues** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Lesen von XML-Werten aus dem SolutionXML-Element (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
