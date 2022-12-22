---
title: Holen Sie sich das Master-Objekt aus dem Zeichnen in PHP
type: docs
weight: 20
url: /de/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram – Abrufen eines Master-Objekts nach ID**
 So erhalten Sie ein Master-Objekt nach ID mit**Aspose.Diagram Java für PHP** , Anruf**get_master_object_by_id** Methode von**GetMasterObject** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Aspose.Diagram – Abrufen eines Master-Objekts nach Name**
 So erhalten Sie ein Master-Objekt anhand des Namens mit**Aspose.Diagram Java für PHP** , Anruf**get_master_object_by_name** Methode von**GetMasterObject** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Master-Objekt aus Zeichnung abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
