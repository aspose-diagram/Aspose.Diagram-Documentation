---
title: Ottieni l'oggetto principale dal disegno in PHP
type: docs
weight: 20
url: /it/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - Ottenere un oggetto master per ID**
 Per ottenere un oggetto master per ID utilizzando**Aspose.Diagram Java per PHP** , chiamata**get_master_object_by_id** metodo di**OttieniOggettoMaster** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# Get master object by id

$master = $diagram->getMasters()->getMaster($master_id);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Ottenere un oggetto principale per nome**
 Per ottenere un oggetto master per nome utilizzando**Aspose.Diagram Java per PHP** , chiamata**get_master_object_by_name** metodo di**OttieniOggettoMaster** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# Get master object by name

$master = $diagram->getMasters()->getMasterByName($master_name);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Ottieni oggetto principale dal disegno (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
