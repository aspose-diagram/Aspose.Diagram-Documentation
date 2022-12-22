---
title: Recupera le informazioni sui master in PHP
type: docs
weight: 30
url: /it/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - Recuperare le Informazioni sui Maestri**
 Per recuperare le informazioni sui master utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**GetMasterInfo** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera le informazioni sui master (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
