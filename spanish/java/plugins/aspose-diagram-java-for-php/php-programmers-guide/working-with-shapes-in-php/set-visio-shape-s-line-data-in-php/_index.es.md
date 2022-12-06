---
title: Establezca los datos de línea de Visio Shape en PHP
type: docs
weight: 140
url: /es/java/set-visio-shape-s-line-data-in-php/
---
## **Aspose.Diagram - Establecer Visio datos de línea de forma**
 Para configurar los datos de línea de la forma Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**EstablecerFormaLíneaDatos** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && (int)(string)$shape->getID() == 1) {

$shape->getLine()->getLineColor()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(1)->getFill()->getFillForegnd()->getValue());

$shape->getLine()->getLineWeight()->setValue(0.07041666666666667);

$shape->getLine()->getRounding()->setValue(0.1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeLineData.vdx", $saveFileFormat->VDX);

print "Set visio shape's line data.".PHP_EOL;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Establecer Visio datos de línea de forma (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeLineData.php)
