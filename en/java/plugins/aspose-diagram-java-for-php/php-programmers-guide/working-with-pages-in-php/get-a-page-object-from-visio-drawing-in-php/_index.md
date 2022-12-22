---
title: Get a Page Object from Visio Drawing in PHP
type: docs
weight: 10
url: /java/get-a-page-object-from-visio-drawing-in-php/
---

## **Aspose.Diagram - Getting a Page Object by ID**
To Get a Page Object by ID using **Aspose.Diagram Java for PHP**, call **get_page_object_by_id** method of **GetPageObject** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function get_page_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$page_id = 0;

\# Get page object by id

$page = $diagram->getPages()->getPage($page_id);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Getting a Page Object by Name**
To Get a Page Object by Name using **Aspose.Diagram Java for PHP**, call **get_page_object_by_name** method of **GetPageObject** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Download Running Code**
Download **Get a Page Object from Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
