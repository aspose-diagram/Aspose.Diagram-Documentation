---
title: Agregar hipervínculo a una forma Visio en PHP
type: docs
weight: 10
url: /es/java/add-hyperlink-to-a-visio-shape-in-php/
---
## **Aspose.Diagram - Agregar hipervínculo**
 Para agregar un hipervínculo usando**Aspose.Diagram Java para PHP** , simplemente invocar**Agregar hipervínculo a forma** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# Initialize Hyperlink object

$hyperlink = new Hyperlink();

\# Set address value

$hyperlink->getAddress()->setValue("http://www.google.com/");

\# Set sub address value

$hyperlink->getSubAddress()->setValue("Sub address here");

\# Set description value

$hyperlink->getDescription()->setValue("Description here");

\# Set name

$hyperlink->setName("MyHyperLink");

\# Add hyperlink to the shape

$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1)->getHyperlinks()->add($hyperlink);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "Hyperlinks.vdx", $saveFileFormat->VDX);

print "Added hyperlik to shape successfully!".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Agregar hipervínculo a una forma Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/AddHyperlinkToShape.php)
