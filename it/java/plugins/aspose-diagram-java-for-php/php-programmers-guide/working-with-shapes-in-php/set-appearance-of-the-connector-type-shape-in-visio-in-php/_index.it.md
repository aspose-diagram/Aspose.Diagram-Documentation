---
title: Impostare l'aspetto della forma del tipo di connettore in Visio in PHP
type: docs
weight: 100
url: /it/java/set-appearance-of-the-connector-type-shape-in-visio-in-php/
---
## **Aspose.Diagram - Impostare l'aspetto della forma del tipo di connettore in Visio**
 Per impostare l'aspetto della forma del tipo di connettore in Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**ImpostaFormaAspetto** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Impostare l'aspetto della forma del tipo di connettore in Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)
