---
title: Recuperar celdas definidas por el usuario de Shapesheet en PHP
type: docs
weight: 30
url: /es/java/retrieve-user-defined-cells-from-shapesheet-in-php/
---
## **Aspose.Diagram - Recuperar celdas definidas por el usuario de Shapesheet**
 Para recuperar celdas definidas por el usuario de Shapesheet usando**Aspose.Diagram Java para PHP** , simplemente invocar**Obtener celdas definidas por el usuario** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir . "drawing.vdx");

$pages=$diagram->getPages();

$count=0;

while($count<(int)(string)$pages->getCount()) {

$page = $pages->get($count);

$shapes = $page->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process") {

$users = $shape->getUsers();

$j = 0;

while ($j<(int)(string)$users->getCount()) {

$user = $users->get($j);

print "Name: " . $user->getNameU() . " Value: " . $user->getValue()->getVal() . " Prompt: " . $user->getPrompt()->getValue();

$j += 1;

}

break;

}

$i += 1;

}

$count += 1;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar celdas definidas por el usuario de Shapesheet (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)
