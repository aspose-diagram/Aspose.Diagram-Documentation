---
title: Seleccione la opción de redirección de la forma del conector en PHP
type: docs
weight: 90
url: /es/java/select-reroute-option-of-the-connector-shape-in-php/
---
## **Aspose.Diagram - Seleccione la opción de redirección de la forma del conector**
 Para seleccionar la opción de redirección de la forma del conector usando**Aspose.Diagram Java para rubí** , simplemente invocar**Seleccionar opción de redirección** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set reroute option

$conFixedCodeValue=new ConFixedCodeValue();

$shape->getLayout()->getConFixedCode()->setValue($conFixedCodeValue->NEVER_REROUTE);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SelectRerouteOption.vdx", $saveFileFormat->VDX);

print "Seleted reroute option of the connector shape.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Seleccione la opción de redirección de la forma del conector (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SelectRerouteOption.php)
