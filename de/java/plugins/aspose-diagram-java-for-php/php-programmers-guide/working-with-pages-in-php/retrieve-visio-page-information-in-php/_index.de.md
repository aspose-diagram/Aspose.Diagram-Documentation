---
title: Rufen Sie Visio-Seiteninformationen in PHP ab
type: docs
weight: 30
url: /de/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - Abrufen von Visio-Seiteninformationen**
 Abrufen von Visio Seiteninformationen mit**Aspose.Diagram Java für PHP** , einfach aufrufen**GetPageInfo** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen von Visio-Seiteninformationen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
