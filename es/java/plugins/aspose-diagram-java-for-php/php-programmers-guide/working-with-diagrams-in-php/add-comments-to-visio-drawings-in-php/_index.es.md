---
title: Agregar comentarios a Visio Dibujos en PHP
type: docs
weight: 10
url: /es/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - Agregar comentarios a Visio Dibujos**
 Para agregar comentarios a Visio Dibujos usando**Aspose.Diagram Java para PHP** , simplemente invocar**AgregarComentarioAlDiagrama** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Add comment

$diagram->getPages()->getPage(0)->addComment(7.205905511811023, 3.880708661417323, "test@");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddComment.vdx", $saveFileFormat->VDX);

print "Added comment successfully!".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Agregar Comentarios a Visio Dibujos (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
