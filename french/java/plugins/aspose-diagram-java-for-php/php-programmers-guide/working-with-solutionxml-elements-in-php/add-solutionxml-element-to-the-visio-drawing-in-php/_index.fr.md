---
title: Ajouter l'élément SolutionXML au dessin Visio en PHP
type: docs
weight: 10
url: /fr/java/add-solutionxml-element-to-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Ajouter un élément SolutionXML au dessin Visio**
 Pour ajouter un élément SolutionXML au dessin Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**AddSolutionXmlElementAddSolutionXmlElement** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Ajouter un élément SolutionXML au dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithSolutionXMLElements/AddSolutionXmlElement.php)
