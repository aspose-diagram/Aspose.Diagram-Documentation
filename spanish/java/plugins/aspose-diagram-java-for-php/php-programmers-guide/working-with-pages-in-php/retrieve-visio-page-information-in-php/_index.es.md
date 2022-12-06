---
title: Recuperar información de la página Visio en PHP
type: docs
weight: 30
url: /es/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - Recuperar Visio Información de la página**
 Para recuperar la información de la página Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**ObtenerInfoPágina** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar Visio Información de página (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
