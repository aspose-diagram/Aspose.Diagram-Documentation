---
title: Wählen Sie die Reroute-Option des Connector-Shapes in PHP
type: docs
weight: 90
url: /de/java/select-reroute-option-of-the-connector-shape-in-php/
---
## **Aspose.Diagram - Wählen Sie die Umleitungsoption der Verbinderform aus**
 Um die Umleitungsoption der Verbinderform auszuwählen, verwenden Sie**Aspose.Diagram Java für Rubin** , einfach aufrufen**Wählen Sie Umleitungsoption** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set reroute option

$conFixedCodeValue=new ConFixedCodeValue();

$shape->getLayout()->getConFixedCode()->setValue($conFixedCodeValue->NEVER_REROUTE);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SelectRerouteOption.vdx", $saveFileFormat->VDX);

print "Seleted reroute option of the connector shape.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Wählen Sie die Umleitungsoption der Verbinderform (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SelectRerouteOption.php)
