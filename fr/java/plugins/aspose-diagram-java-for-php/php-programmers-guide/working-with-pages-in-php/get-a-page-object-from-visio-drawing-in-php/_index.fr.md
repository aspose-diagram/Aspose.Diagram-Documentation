---
title: Obtenir un objet de page à partir du dessin Visio en PHP
type: docs
weight: 10
url: /fr/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - Obtention d'un objet de page par ID**
 Pour obtenir un objet de page par ID à l'aide de**Aspose.Diagram Java pour PHP** , appel**get_page_object_by_id** méthode de**GetPageObject** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 public static function get_page_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$page_id = 0;

\# Get page object by id

$page = $diagram->getPages()->getPage($page_id);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Obtenir un objet de page par nom**
 Pour obtenir un objet de page par nom à l'aide**Aspose.Diagram Java pour PHP** , appel**get_page_object_by_name** méthode de**GetPageObject** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 public static function get_page_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set page name

$page_name = "Flow 1";

\# Get page object by name

$page = $diagram->getPages()->getPage($page_name);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Obtenir un objet de page à partir du dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
