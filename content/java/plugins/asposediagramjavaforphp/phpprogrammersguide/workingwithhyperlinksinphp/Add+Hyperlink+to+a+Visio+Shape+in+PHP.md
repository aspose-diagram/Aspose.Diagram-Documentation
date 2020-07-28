+++
title = "Add Hyperlink to a Visio Shape in PHP" 
description = "" 
weight = 20197 
+++

Aspose.Diagram for Java : Add Hyperlink to a Visio Shape in PHP  

# Aspose.Diagram for Java : Add Hyperlink to a Visio Shape in PHP


## Aspose.Diagram - Add Hyperlink

To Add Hyperlink using **Aspose.Diagram Java for PHP**, simply invoke **AddHyperlinkToShape** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir . "Drawing.vsd");

# Initialize Hyperlink object
$hyperlink = new Hyperlink();

# Set address value
$hyperlink->getAddress()->setValue("http://www.google.com/");

# Set sub address value
$hyperlink->getSubAddress()->setValue("Sub address here");

# Set description value
$hyperlink->getDescription()->setValue("Description here");

# Set name
$hyperlink->setName("MyHyperLink");

# Add hyperlink to the shape
$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1)->getHyperlinks()->add($hyperlink);

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir . "Hyperlinks.vdx", $saveFileFormat->VDX);

print "Added hyperlik to shape successfully!".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Add Hyperlink to a Visio Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/AddHyperlinkToShape.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithHyperlinks/AddHyperlinkToShape.php)

