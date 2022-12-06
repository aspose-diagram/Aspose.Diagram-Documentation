---
title: Ottieni un oggetto pagina da Visio Disegno in PHP
type: docs
weight: 10
url: /it/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - Ottenere un oggetto della pagina per ID**
 Per ottenere un oggetto pagina per ID utilizzando**Aspose.Diagram Java per PHP** , chiamata**get_page_object_by_id** metodo di**OttieniOggettoPagina** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Aspose.Diagram - Ottenere un oggetto pagina per nome**
 Per ottenere un oggetto pagina per nome utilizzando**Aspose.Diagram Java per PHP** , chiamata**get_page_object_by_name** metodo di**OttieniOggettoPagina** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Ottieni un oggetto pagina dal disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
