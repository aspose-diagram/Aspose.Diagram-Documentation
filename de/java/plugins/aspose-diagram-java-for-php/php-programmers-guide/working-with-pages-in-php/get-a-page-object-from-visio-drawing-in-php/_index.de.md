---
title: Holen Sie sich ein Seitenobjekt von Visio Drawing in PHP
type: docs
weight: 10
url: /de/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram – Abrufen eines Seitenobjekts nach ID**
 So erhalten Sie ein Seitenobjekt nach ID mit**Aspose.Diagram Java für PHP** , Anruf**get_page_object_by_id** Methode von**GetPageObject** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 public static function get_page_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$page_id = 0;

\# Get page object by id

$page = $diagram->getPages()->getPage($page_id);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram – Abrufen eines Seitenobjekts nach Name**
 So erhalten Sie ein Seitenobjekt anhand des Namens mit**Aspose.Diagram Java für PHP** , Anruf**get_page_object_by_name** Methode von**GetPageObject** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 public static function get_page_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set page name

$page_name = "Flow 1";

\# Get page object by name

$page = $diagram->getPages()->getPage($page_name);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen eines Seitenobjekts aus Visio-Zeichnung (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
