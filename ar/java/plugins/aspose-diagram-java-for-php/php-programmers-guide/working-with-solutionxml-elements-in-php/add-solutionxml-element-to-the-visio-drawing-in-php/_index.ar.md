---
title: أضف عنصر SolutionXML إلى رسم Visio في PHP
type: docs
weight: 10
url: /ar/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram - إضافة SolutionXML Element إلى رسم Visio**
 لإضافة عنصر SolutionXML إلى رسم Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**AddSolutionXmlElement** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **قم بتنزيل كود التشغيل**
 تحميل**أضف عنصر SolutionXML إلى رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
