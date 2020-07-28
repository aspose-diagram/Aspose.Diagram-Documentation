+++
title = "Create User-defined Cell in the ShapeSheet in PHP" 
description = "" 
weight = 20233 
+++

Aspose.Diagram for Java : Create User-defined Cell in the ShapeSheet in PHP  

# Aspose.Diagram for Java : Create User-defined Cell in the ShapeSheet in PHP


## Aspose.Diagram - Create User-defined Cell in the ShapeSheet

To Create User-defined Cell in the ShapeSheet using **Aspose.Diagram Java for PHP**, simply invoke **CreateUserDefinedCell** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram=new Diagram($dataDir . "Drawing.vsd");

$pages=$diagram->getPages();

$i=0;
while($i<(int)(string)$pages->getCount()) {
$page = $pages->get($i);
$shapes = $page->getShapes();
$j = 0;
while ($j<(int)(string)$shapes->getCount()) {
$shape = $shapes->get($j);
if ($shape->getNameU() == "Process") {
# Initialize user object
$user = new User();
$user->setName("UserDefineCell");
$user->getValue()->setVal("800");

# Add user-defined cell
$shape->getUsers()->add($user);
}
$j += 1;
}
$i += 1;
}

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir . "UserDefinedCells.vdx", $saveFileFormat->VDX);
print "Created User-defined Cell in the ShapeSheet.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Create User-defined Cell in the ShapeSheet (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)

