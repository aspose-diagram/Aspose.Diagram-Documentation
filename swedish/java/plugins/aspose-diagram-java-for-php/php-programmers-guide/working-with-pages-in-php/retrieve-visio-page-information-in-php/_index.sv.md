---
title: Hämta Visio Sidinformation i PHP
type: docs
weight: 30
url: /sv/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - Hämta Visio Sidinformation**
 För att hämta Visio Sidinformation med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetPageInfo** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Visio Sidinformation (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
