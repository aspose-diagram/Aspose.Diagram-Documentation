---
title: Cree un Visio Diagram vacío en PHP
type: docs
weight: 20
url: /es/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - Crear un vacío Visio Diagram**
 Para crear un Visio Diagram vacío usando**Aspose.Diagram Java para PHP** , simplemente invocar**CrearDiagrama** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Cree un Visio Diagram (Aspose.Diagram) vacío**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
