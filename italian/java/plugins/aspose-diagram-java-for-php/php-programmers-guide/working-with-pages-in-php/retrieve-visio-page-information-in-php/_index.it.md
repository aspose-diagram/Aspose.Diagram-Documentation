---
title: Recupera le informazioni sulla pagina Visio in PHP
type: docs
weight: 30
url: /it/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - Recupera Visio Informazioni Pagina**
 Per recuperare le informazioni sulla pagina Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**OttieniInfoPagina** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera Visio Informazioni sulla pagina (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
