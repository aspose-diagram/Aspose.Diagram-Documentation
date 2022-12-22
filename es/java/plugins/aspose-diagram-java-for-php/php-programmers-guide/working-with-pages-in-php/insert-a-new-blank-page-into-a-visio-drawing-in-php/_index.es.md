---
title: Inserte una nueva página en blanco en un dibujo Visio en PHP
type: docs
weight: 20
url: /es/java/insert-a-new-blank-page-into-a-visio-drawing-in-php/
---
## **Aspose.Diagram - Insertar una nueva página en blanco en un dibujo Visio**
 Para insertar una nueva página en blanco en un dibujo Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**Añadir página** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Insertar una nueva página en blanco en un dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/AddPage.php)
