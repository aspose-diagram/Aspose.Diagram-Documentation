---
title: Rufen Sie Informationen zu Zeichnungsschriften in PHP ab
type: docs
weight: 40
url: /de/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram – Abrufen von Zeichensatzinformationen**
 So rufen Sie Informationen zu Zeichnungsschriften ab**Aspose.Diagram Java für PHP** , einfach aufrufen**GetDiagramFontInfo** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$fonts = $diagram->getFonts();

$i = 0;

while ($i<sizeof($fonts->getCount())) {

$font = $fonts->get($i);

\# Display information about the fonts

print $font->getName();

$i+=1;

}

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Zeichnungsschriftinformationen abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
