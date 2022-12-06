---
title: Sélectionnez l'option de redirection de la forme du connecteur en PHP
type: docs
weight: 90
url: /fr/java/select-reroute-option-of-the-connector-shape-in-php/
---
## **Aspose.Diagram - Sélectionnez l'option de réacheminement de la forme du connecteur**
 Pour sélectionner l'option de réacheminement de la forme du connecteur à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**SelectRerouteOption** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set reroute option

$conFixedCodeValue=new ConFixedCodeValue();

$shape->getLayout()->getConFixedCode()->setValue($conFixedCodeValue->NEVER_REROUTE);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SelectRerouteOption.vdx", $saveFileFormat->VDX);

print "Seleted reroute option of the connector shape.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Sélectionnez l'option de réacheminement de la forme du connecteur (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SelectRerouteOption.php)
