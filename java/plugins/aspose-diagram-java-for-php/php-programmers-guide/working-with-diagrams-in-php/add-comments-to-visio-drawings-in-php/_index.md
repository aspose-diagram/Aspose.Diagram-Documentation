---
title: Add Comments to Visio Drawings in PHP
type: docs
weight: 10
url: /java/add-comments-to-visio-drawings-in-php/
---

## **Aspose.Diagram - Add Comments to Visio Drawings**
To Add Comments to Visio Drawings using **Aspose.Diagram Java for PHP**, simply invoke **AddCommentToDiagram** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Add comment

$diagram->getPages()->getPage(0)->addComment(7.205905511811023, 3.880708661417323, "test@");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddComment.vdx", $saveFileFormat->VDX);

print "Added comment successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Add Comments to Visio Drawings (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
- [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
