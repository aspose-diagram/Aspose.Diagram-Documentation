---
title: Lettura di valori XML dall'elemento SolutionXML in PHP
type: docs
weight: 20
url: /it/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram - Lettura di valori XML dall'elemento SolutionXML**
 Per leggere i valori XML dall'elemento SolutionXML utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**ReadXmlValues** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Lettura di valori XML dall'elemento SolutionXML (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
