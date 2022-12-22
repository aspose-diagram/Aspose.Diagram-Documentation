---
title: PHP'de SolutionXML Öğesinden XML Değerlerini Okuma
type: docs
weight: 20
url: /tr/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram - SolutionXML Öğesinden XML Değerlerini Okuma**
 SolutionXML Öğesinden XML Değerlerini Okumak için**PHP için Aspose.Diagram Java** , sadece çağırmak**ReadXmlValues** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**SolutionXML Öğesinden XML Değerlerini Okuma (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
