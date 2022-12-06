---
title: Добавьте элемент SolutionXML в чертеж Visio в PHP
type: docs
weight: 10
url: /ru/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram — добавление элемента SolutionXML в чертеж Visio**
 Чтобы добавить элемент SolutionXML в чертеж Visio с помощью**Aspose.Diagram Java для PHP** , просто вызовите**AddSolutionXmlElement** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Добавьте элемент SolutionXML в чертеж Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
