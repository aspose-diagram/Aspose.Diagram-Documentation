---
title: Récupérer les informations de la page Visio en PHP
type: docs
weight: 30
url: /fr/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - Récupérer les informations de la page Visio**
 Pour récupérer les informations de la page Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**GetPageInfo** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations de la page Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
