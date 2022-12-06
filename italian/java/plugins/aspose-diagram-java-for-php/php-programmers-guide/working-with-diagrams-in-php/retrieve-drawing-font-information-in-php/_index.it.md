---
title: Recupera le informazioni sui caratteri del disegno in PHP
type: docs
weight: 40
url: /it/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - Recupera informazioni sui caratteri del disegno**
 Per recuperare le informazioni sui caratteri del disegno utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**OttieniDiagramFontInfo** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Recupera informazioni sui caratteri del disegno (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
