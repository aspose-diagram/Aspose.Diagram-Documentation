---
title: Hämta information om ritningsteckensnitt i PHP
type: docs
weight: 40
url: /sv/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - Hämta information om ritningsteckensnitt**
 För att hämta information om ritningsteckensnitt med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetDiagramFontInfo** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Hämta information om ritningsteckensnitt (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
