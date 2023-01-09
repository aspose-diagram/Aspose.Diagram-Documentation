---
title: Inserisci una nuova pagina vuota in un disegno Visio in PHP
type: docs
weight: 20
url: /it/java/insert-a-new-blank-page-into-a-visio-drawing-in-php/
---
## **Aspose.Diagram - Inserimento di una nuova pagina vuota in un disegno Visio**
 Per inserire una nuova pagina vuota in un disegno Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Aggiungi pagina** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Get max page ID

$max_page_id = $diagram->getPages()->getPage(0)->getID();

$i = 1;

while ($i<(int)(string)$diagram->getPages()->getCount()) {

if ($max_page_id<$diagram->getPages()->getPage($i)->getID()){

$max_page_id=$diagram->getPages()->getPage($i)->getID();

}

$i+=1;

}

\# Initialize a new page object

$new_page = new Page();

\# Set name

$new_page->setName("new page");

\# Set page ID

$new_page->setID((int)(string)$max_page_id+1);

\# Or try the Page constructor

\# Page newPage = new Page(MaxPageId + 1);

\# Add a new blank page

$diagram->getPages()->add($new_page);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."NewPage_Output.vdx", $saveFileFormat->VDX);

print "Added new page.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Inserisci una nuova pagina vuota in un disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/AddPage.php)
