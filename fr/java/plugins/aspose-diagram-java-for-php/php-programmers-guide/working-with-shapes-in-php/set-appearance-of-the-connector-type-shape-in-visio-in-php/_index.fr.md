---
title: Définir l'apparence de la forme du type de connecteur dans Visio en PHP
type: docs
weight: 100
url: /fr/java/set-appearance-of-the-connector-type-shape-in-visio-in-php/
---
## **Aspose.Diagram - Définir l'apparence de la forme du type de connecteur dans Visio**
 Pour définir l'apparence de la forme du type de connecteur dans Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**DéfinirApparenceForme** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set dynamic connector appearance

$connectorsTypeValue=new ConnectorsTypeValue();

$shape->setConnectorsType($connectorsTypeValue->STRAIGHT_LINES);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeAppearance.vdx",$saveFileFormat->VDX);

print "Set appearnce of the connector type shape.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Définir l'apparence de la forme du type de connecteur dans Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)
