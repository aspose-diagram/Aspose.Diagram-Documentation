---
title: Obtenga el objeto maestro del dibujo en PHP
type: docs
weight: 20
url: /es/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - Obtención de un objeto maestro por ID**
 Para obtener un objeto maestro por ID usando**Aspose.Diagram Java para PHP** , llamar**get_master_object_by_id** método de**ObtenerObjetoMaestro** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# Get master object by id

$master = $diagram->getMasters()->getMaster($master_id);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Obtención de un objeto maestro por nombre**
 Para obtener un objeto maestro por nombre usando**Aspose.Diagram Java para PHP** , llamar**get_master_object_by_name** método de**ObtenerObjetoMaestro** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# Get master object by name

$master = $diagram->getMasters()->getMasterByName($master_name);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Obtener objeto maestro del dibujo (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
