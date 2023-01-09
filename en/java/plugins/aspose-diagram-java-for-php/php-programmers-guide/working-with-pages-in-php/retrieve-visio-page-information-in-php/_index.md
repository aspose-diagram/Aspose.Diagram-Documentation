---
title: Retrieve Visio Page Information in PHP
type: docs
weight: 30
url: /java/retrieve-visio-page-information-in-php/
---

## **Aspose.Diagram - Retrieve Visio Page Information**
To Retrieve Visio Page Information using **Aspose.Diagram Java for PHP**, simply invoke **GetPageInfo** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

#page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve Visio Page Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
