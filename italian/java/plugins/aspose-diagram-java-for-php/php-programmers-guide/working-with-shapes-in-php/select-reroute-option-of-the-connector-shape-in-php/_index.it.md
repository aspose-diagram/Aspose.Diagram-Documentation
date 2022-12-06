---
title: Seleziona Reindirizza opzione della forma del connettore in PHP
type: docs
weight: 90
url: /it/java/select-reroute-option-of-the-connector-shape-in-php/
---
## **Aspose.Diagram - Selezionare l'opzione di reindirizzamento della forma del connettore**
 Per selezionare l'opzione di reindirizzamento della forma del connettore utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**Selezionare Reindirizza opzione** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Selezionare l'opzione di reindirizzamento della forma del connettore (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SelectRerouteOption.php)
