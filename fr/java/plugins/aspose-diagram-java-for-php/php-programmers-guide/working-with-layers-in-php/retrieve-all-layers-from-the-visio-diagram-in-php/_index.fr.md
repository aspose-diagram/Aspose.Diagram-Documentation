---
title: Récupérer toutes les couches du Visio Diagram en PHP
type: docs
weight: 20
url: /fr/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Récupérer toutes les couches**
 Pour récupérer tous les calques à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**Obtenir toutes les couches** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# get Visio page

$page=$diagram->getPages()->getPage(0);

$layers=$page->getPageSheet()->getLayers();

$i = 0;

while ($i<(int)(string)$layers->getCount()) {

$layer=$layers->get($i);

print "Name: " . (string)$layer->getName()->getValue();

print "Visibility: " . (string)$layer->getVisible()->getValue();

print "Status: " . (string)$layer->getStatus()->getValue();

$i += 1;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer toutes les couches du Visio Diagram (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
