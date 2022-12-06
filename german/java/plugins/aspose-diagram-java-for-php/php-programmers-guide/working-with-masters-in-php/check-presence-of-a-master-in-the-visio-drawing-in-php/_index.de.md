---
title: Überprüfen Sie das Vorhandensein eines Masters in der Visio-Zeichnung in PHP
type: docs
weight: 10
url: /de/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram – Überprüfen einer Master-Anwesenheit anhand der ID**
 So überprüfen Sie eine Master-Anwesenheit anhand der ID mit**Aspose.Diagram Java für PHP** , Anruf**check_presence_master_by_id** Methode von**CheckPresenceOfMaster** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Aspose.Diagram – Überprüfung einer Master-Anwesenheit anhand des Namens**
 So überprüfen Sie eine Master-Anwesenheit anhand des Namens mit**Aspose.Diagram Java für PHP** , Anruf**check_presence_master_by_name** Methode von**CheckPresenceOfMaster** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Überprüfen Sie das Vorhandensein eines Masters in der Visio-Zeichnung (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
