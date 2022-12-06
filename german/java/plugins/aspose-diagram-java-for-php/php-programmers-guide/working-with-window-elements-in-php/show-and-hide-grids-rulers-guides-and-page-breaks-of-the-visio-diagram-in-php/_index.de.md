---
title: Gitter, Lineale, Hilfslinien und Seitenumbrüche von Visio Diagram in PHP ein- und ausblenden
type: docs
weight: 40
url: /de/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Gitter, Lineale, Hilfslinien und Seitenumbrüche von Visio Diagram ein- und ausblenden**
Zum Ein- und Ausblenden von Rastern, Linealen, Hilfslinien und Seitenumbrüchen der Visio Diagram mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ShowHideProperties** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# set visibility of grid

$window->setShowGrid(1);

\# set visibility of guides

$window->setShowGuides(1);

\# set visibility of rulers

$window->setShowRulers(1);

\# set visibility of page breaks

$window->setShowPageBreaks(1);

\# save in any supported format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ShowHideProperties.vdx", $saveFileFormat->VDX);

print "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Raster, Lineale, Hilfslinien und Seitenumbrüche von Visio Diagram (Aspose.Diagram) ein- und ausblenden**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/ShowHideProperties.php)
