---
title: Obtenga un objeto de página de Visio Dibujo en PHP
type: docs
weight: 10
url: /es/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - Obtener un objeto de página por ID**
 Para obtener un objeto de página por ID usando**Aspose.Diagram Java para PHP** , llamar**get_page_object_by_id** método de**ObtenerObjetoPágina** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Aspose.Diagram - Obtener un objeto de página por nombre**
 Para obtener un objeto de página por nombre usando**Aspose.Diagram Java para PHP** , llamar**get_page_object_by_name** método de**ObtenerObjetoPágina** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Obtenga un objeto de página del dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
