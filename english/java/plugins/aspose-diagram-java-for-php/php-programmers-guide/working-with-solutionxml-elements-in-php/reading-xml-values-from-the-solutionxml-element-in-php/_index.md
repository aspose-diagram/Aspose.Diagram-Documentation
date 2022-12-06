---
title: Reading XML Values from the SolutionXML Element in PHP
type: docs
weight: 20
url: /java/reading-xml-values-from-the-solutionxml-element-in-php/
---

## **Aspose.Diagram - Reading XML Values from the SolutionXML Element**
To Reading XML Values from the SolutionXML Element using **Aspose.Diagram Java for PHP**, simply invoke **ReadXmlValues** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Download Running Code**
Download **Reading XML Values from the SolutionXML Element (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
