---
title: Verificare la presenza di un master nel disegno Visio in PHP
type: docs
weight: 10
url: /it/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Controllo Presenza Master tramite ID**
 Per controllare una presenza principale tramite ID utilizzando**Aspose.Diagram Java per PHP** , chiamata**check_presence_master_by_id** metodo di**CheckPresenceOfMaster** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 public static function check_presence_master_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# check master by id

$is_present = $diagram->getMasters()->isExist($master_id);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Controllo Presenza Master per Nome**
 Per controllare una presenza principale per nome utilizzando**Aspose.Diagram Java per PHP** , chiamata**check_presence_master_by_name** metodo di**CheckPresenceOfMaster** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 public static function check_presence_master_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# check master object by name

$is_present = $diagram->getMasters()->isExist($master_name);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Verifica Presenza Master nel Disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
