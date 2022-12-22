---
title: Aggiungi commenti a Visio Disegni in PHP
type: docs
weight: 10
url: /it/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - Aggiungi commenti a Visio Disegni**
 Per aggiungere commenti ai disegni Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**AddCommentToDiagram** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Aggiungi commenti a Visio Disegni (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
