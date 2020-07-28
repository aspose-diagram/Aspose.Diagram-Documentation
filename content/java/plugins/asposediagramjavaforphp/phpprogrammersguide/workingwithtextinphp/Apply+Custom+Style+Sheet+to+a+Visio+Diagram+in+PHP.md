+++
title = "Apply Custom Style Sheet to a Visio Diagram in PHP" 
description = "" 
weight = 20229 
+++

Aspose.Diagram for Java : Apply Custom Style Sheet to a Visio Diagram in PHP  

# Aspose.Diagram for Java : Apply Custom Style Sheet to a Visio Diagram in PHP


## Aspose.Diagram - Apply Custom Style Sheet to a Visio Diagram

To Apply Custom Style Sheet to a Visio Diagram using **Aspose.Diagram Java for PHP**, simply invoke **ApplyCustomStyleSheet** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes =$diagram->getPages()->getPage(0)->getShapes();

$i=0;
while ($i<(int)(string)$shapes->getCount()) {
$shape=$shapes->get($i);
if($shape->getNameU()=="Process") {
$source_shape =$shape;
break;
}
$i+= 1;
}

# Find the required style sheet
$stylesheets=$diagram->getStyleSheets();
$j=0;
while($j<(int)(string)$stylesheets->getCount()) {
$stylesheet=$stylesheets->get($j);
if($stylesheet->getName() == "Basic") {
$custom_stylesheet = $stylesheet;
break;
}
$j+= 1;
}

if ($source_shape!=null && $custom_stylesheet !=null) {
# Apply text style
$source_shape->setTextStyle($custom_stylesheet);
# Apply fill style
$source_shape->setFillStyle($custom_stylesheet);
# Apply line style
$source_shape->setLineStyle($custom_stylesheet);
}

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."ApplyCustomStyleSheet.vdx", $saveFileFormat->VDX);

print "Applied custom stylesheet to a visio diagram.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Apply Custom Style Sheet to a Visio Diagram (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/ApplyCustomStyleSheet.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithText/ApplyCustomStyleSheet.php)

