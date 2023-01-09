---
title: Kommentare zu Visio Zeichnungen in PHP hinzufügen
type: docs
weight: 10
url: /de/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - Kommentare zu Visio Zeichnungen hinzufügen**
 Um Kommentare zu Visio-Zeichnungen hinzuzufügen, verwenden Sie**Aspose.Diagram Java für PHP** , einfach aufrufen**AddCommentToDiagram** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Kommentare zu Visio Zeichnungen hinzufügen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
