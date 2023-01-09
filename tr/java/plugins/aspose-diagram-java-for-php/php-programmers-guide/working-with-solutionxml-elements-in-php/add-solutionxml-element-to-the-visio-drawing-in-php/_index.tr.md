---
title: PHP'de Visio Çizimine SolutionXML Öğesi Ekleyin
type: docs
weight: 10
url: /tr/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Visio Çizimine SolutionXML Öğesi Ekleyin**
 Kullanarak Visio Çizimine SolutionXML Öğesi Eklemek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**AddSolutionXmlElement** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Visio Çizimine (Aspose.Diagram) SolutionXML Öğesi Ekleme**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
