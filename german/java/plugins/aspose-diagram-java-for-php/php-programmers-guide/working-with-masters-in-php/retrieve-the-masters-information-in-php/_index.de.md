---
title: Rufen Sie die Masterinformationen in PHP ab
type: docs
weight: 30
url: /de/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - Rufen Sie die Masterinformationen ab**
 So rufen Sie die Masters-Informationen ab**Aspose.Diagram Java für PHP** , einfach aufrufen**GetMasterInfo** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen der Masterinformationen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
