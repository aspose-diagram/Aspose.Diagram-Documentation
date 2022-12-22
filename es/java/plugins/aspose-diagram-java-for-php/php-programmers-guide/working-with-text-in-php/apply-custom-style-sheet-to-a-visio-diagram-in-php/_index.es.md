---
title: Aplique una hoja de estilo personalizada a un Visio Diagram en PHP
type: docs
weight: 10
url: /es/java/apply-custom-style-sheet-to-a-visio-diagram-in-php/
---
## **Aspose.Diagram - Aplicar hoja de estilo personalizado a un Visio Diagram**
 Para aplicar una hoja de estilo personalizada a un Visio Diagram usando**Aspose.Diagram Java para PHP** , simplemente invocar**ApplyCustomStyleSheet** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes =$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()) {

$shape=$shapes->get($i);

if($shape->getNameU()=="Process") {

$source_shape =$shape;

break;

}

$i+= 1;

}

\# Find the required style sheet

$stylesheets=$diagram->getStyleSheets();

$j=0;

while($j<(int)(string)$stylesheets->getCount()) {

$stylesheet=$stylesheets->get($j);

if($stylesheet->getName() == "Basic") {

$custom_stylesheet = $stylesheet;

break;

}

$j+= 1;

}

if ($source_shape!=null && $custom_stylesheet !=null) {

\# Apply text style

$source_shape->setTextStyle($custom_stylesheet);

\# Apply fill style

$source_shape->setFillStyle($custom_stylesheet);

\# Apply line style

$source_shape->setLineStyle($custom_stylesheet);

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ApplyCustomStyleSheet.vdx", $saveFileFormat->VDX);

print "Applied custom stylesheet to a visio diagram.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Aplicar hoja de estilo personalizado a un Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/ApplyCustomStyleSheet.php)
