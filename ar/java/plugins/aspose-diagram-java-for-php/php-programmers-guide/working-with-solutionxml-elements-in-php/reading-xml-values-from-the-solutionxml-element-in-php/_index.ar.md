---
title: قراءة قيم XML من SolutionXML Element في PHP
type: docs
weight: 20
url: /ar/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram - قراءة قيم XML من SolutionXML Element**
 لقراءة قيم XML من SolutionXML Element باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ReadXmlValues** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **قم بتنزيل كود التشغيل**
 تحميل**قراءة قيم XML من SolutionXML Element (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
