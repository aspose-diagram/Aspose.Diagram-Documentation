---
title: Fügen Sie das SolutionXML-Element zur Zeichnung Visio in PHP hinzu
type: docs
weight: 10
url: /de/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram – SolutionXML-Element zur Zeichnung Visio hinzugefügt**
 Um das SolutionXML-Element zur Visio-Zeichnung hinzuzufügen, verwenden Sie**Aspose.Diagram Java für PHP** , einfach aufrufen**AddSolutionXmlElement** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."drawing.vsd");

\# initialize SolutionXML object

$solution_xml=new SolutionXML();

\# set name

$solution_xml->setName("Solution XML");

\# set xml value

$solution_xml->setXmlValue("XML Value");

\# add SolutionXML element

$diagram->getSolutionXMLs()->add($solution_xml);

\# save Visio diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SolutionXmlElement.vdx", $saveFileFormat->VDX);

print "Added SolutionXML Element to the Visio Drawing.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**SolutionXML-Element zur Zeichnung Visio hinzufügen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
