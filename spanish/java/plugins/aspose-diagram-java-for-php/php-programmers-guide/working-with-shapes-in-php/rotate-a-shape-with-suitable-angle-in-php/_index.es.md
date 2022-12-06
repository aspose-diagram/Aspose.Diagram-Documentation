---
title: Girar una forma con ángulo adecuado en PHP
type: docs
weight: 80
url: /es/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - Girar una forma con el ángulo adecuado**
 Para rotar una forma con un ángulo adecuado usando**Aspose.Diagram Java para PHP** , simplemente invocar**RotarForma** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Add a shape and set the angle

$diagram->getPages()->getPage(0)->getShapes()->getShape(1)->setAngle(190);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RotateShape.vdx",$saveFileFormat->VDX);

print "Rotated shape.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Girar una forma con ángulo adecuado (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
