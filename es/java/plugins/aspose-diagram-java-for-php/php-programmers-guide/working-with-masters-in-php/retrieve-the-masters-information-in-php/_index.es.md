---
title: Recuperar la información de los maestros en PHP
type: docs
weight: 30
url: /es/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - Recuperar la información de los maestros**
 Para recuperar la información maestra usando**Aspose.Diagram Java para PHP** , simplemente invocar**ObtenerInfoMaestra** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar la información de los maestros (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
