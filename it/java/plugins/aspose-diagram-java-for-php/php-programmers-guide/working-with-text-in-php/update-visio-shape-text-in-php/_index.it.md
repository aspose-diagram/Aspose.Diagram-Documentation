---
title: Aggiorna Visio Forma il testo in PHP
type: docs
weight: 30
url: /it/java/update-visio-shape-text-in-php/
---
## **Aspose.Diagram - Aggiorna Visio Forma testo**
Per aggiornare Visio Forma testo utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**UpdateShapeText** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 1) {

$shape->getText()->getValue()->clear();

$shape->getText()->getValue()->add(new Txt("New Text"));

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."UpdateShapeText.vdx",$saveFileFormat->VDX);

print "Updated shape text.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Aggiorna Visio Forma testo (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/UpdateShapeText.php)
