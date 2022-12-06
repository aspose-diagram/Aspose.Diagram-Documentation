---
title: Récupérer les informations de police de dessin en PHP
type: docs
weight: 40
url: /fr/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - Récupérer les informations sur la police de dessin**
 Pour récupérer les informations sur la police de dessin à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**GetDiagramFontInfo** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations sur la police de dessin (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
