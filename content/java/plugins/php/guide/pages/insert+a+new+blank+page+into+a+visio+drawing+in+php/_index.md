---
title : "Insert a New Blank Page into a Visio Drawing in PHP" 
description : "" 
weight : 20204 
toc : false
type: docs
url: /java/plugins/php/guide/pages/insert+a+new+blank+page+into+a+visio+drawing+in+php/
---

# Aspose.Diagram for Java : Insert a New Blank Page into a Visio Drawing in PHP


## Aspose.Diagram - Insert a New Blank Page into a Visio Drawing

To Insert a New Blank Page into a Visio Drawing using **Aspose.Diagram Java for PHP**, simply invoke **AddPage** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir."drawing.vsd");

# Get max page ID

$max_page_id = $diagram->getPages()->getPage(0)->getID();
$i = 1;
while ($i<(int)(string)$diagram->getPages()->getCount()) {
if ($max_page_id<$diagram->getPages()->getPage($i)->getID()){
$max_page_id=$diagram->getPages()->getPage($i)->getID();
}
$i+=1;
}

# Initialize a new page object
$new_page = new Page();

# Set name
$new_page->setName("new page");

# Set page ID
$new_page->setID((int)(string)$max_page_id+1);

# Or try the Page constructor
# Page newPage = new Page(MaxPageId + 1);

# Add a new blank page
$diagram->getPages()->add($new_page);

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."NewPage_Output.vdx", $saveFileFormat->VDX);
print "Added new page.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Insert a New Blank Page into a Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/AddPage.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithPages/AddPage.php)

