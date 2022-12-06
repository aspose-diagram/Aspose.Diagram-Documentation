---
title: Agregue el elemento SolutionXML al dibujo Visio en PHP
type: docs
weight: 10
url: /es/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Agregar elemento SolutionXML al dibujo Visio**
 Para agregar el elemento SolutionXML al dibujo Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**AddSolutionXmlElementAddSolutionXmlElement** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Agregue el elemento SolutionXML al dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
