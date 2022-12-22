---
title: Чтение значений XML из элемента SolutionXML в PHP
type: docs
weight: 20
url: /ru/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram — Чтение значений XML из элемента SolutionXML**
 Чтение значений XML из элемента SolutionXML с помощью**Aspose.Diagram Java для PHP** , просто вызовите**Реадксмлвалуерес** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Чтение значений XML из элемента SolutionXML (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
