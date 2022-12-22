---
title: Visa och dölj rutnät, linjaler, guider och sidbrytningar av Visio Diagram i PHP
type: docs
weight: 40
url: /sv/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Visa och dölj rutnät, linjaler, guider och sidbrytningar i Visio Diagram**
Att visa och dölja rutnät, linjaler, guider och sidbrytningar i Visio Diagram med**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ShowHideProperties** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Visa och dölj rutnät, linjaler, guider och sidbrytningar i Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/ShowHideProperties.php)
