---
title: Eliminar todas las macros del Visio Diagram en PHP
type: docs
weight: 30
url: /es/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Eliminar todas las macros del Visio Diagram**
 Para quitar todas las macros del Visio Diagram usando**Aspose.Diagram Java para PHP** , simplemente invocar**Quitar todas las macros del diagrama** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Eliminar todas las macros del Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
