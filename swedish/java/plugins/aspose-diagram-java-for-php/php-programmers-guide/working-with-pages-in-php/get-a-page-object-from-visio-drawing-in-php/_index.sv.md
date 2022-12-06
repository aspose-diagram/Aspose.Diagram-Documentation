---
title: Skaffa ett sidobjekt från Visio Rita i PHP
type: docs
weight: 10
url: /sv/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - Hämta ett sidobjekt med ID**
 För att få ett sidobjekt efter ID med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**get_page_object_by_id** metod av**GetPageObject** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Aspose.Diagram - Få ett sidobjekt efter namn**
 För att få ett sidobjekt efter namn med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**get_page_object_by_name** metod av**GetPageObject** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Skaffa ett sidobjekt från Visio Drawing (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
