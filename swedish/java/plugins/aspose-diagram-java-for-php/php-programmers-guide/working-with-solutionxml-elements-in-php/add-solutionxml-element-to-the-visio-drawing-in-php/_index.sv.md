---
title: Lägg till SolutionXML Element till Visio-ritningen i PHP
type: docs
weight: 10
url: /sv/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Lägg till SolutionXML Element till Visio-ritningen**
 För att lägga till SolutionXML Element till Visio-ritningen med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**AddSolutionXmlElement** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Lägg till SolutionXML Element till Visio-ritningen (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
