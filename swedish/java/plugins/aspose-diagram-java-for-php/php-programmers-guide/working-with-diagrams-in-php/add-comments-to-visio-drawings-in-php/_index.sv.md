---
title: Lägg till kommentarer till Visio Ritningar i PHP
type: docs
weight: 10
url: /sv/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - Lägg till kommentarer till Visio ritningar**
 För att lägga till kommentarer till Visio Ritningar med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**AddCommentToDiagram** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Lägg till kommentarer till Visio Ritningar (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
