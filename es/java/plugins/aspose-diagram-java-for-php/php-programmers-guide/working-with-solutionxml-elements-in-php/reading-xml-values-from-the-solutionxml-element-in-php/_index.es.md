---
title: Lectura de valores XML del elemento SolutionXML en PHP
type: docs
weight: 20
url: /es/java/reading-xml-values-from-the-solutionxml-element-in-php/
---
## **Aspose.Diagram - Lectura de valores XML del elemento SolutionXML**
 Para leer valores XML del elemento SolutionXML usando**Aspose.Diagram Java para PHP** , simplemente invocar**Leer valores Xml** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Lectura de valores XML del elemento SolutionXML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/ReadXmlValues.php)
