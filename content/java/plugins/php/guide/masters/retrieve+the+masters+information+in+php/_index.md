---
title : "Retrieve the Masters Information in PHP" 
description : "" 
weight : 20185 
toc : false
type: docs
url: /java/plugins/php/guide/masters/retrieve+the+masters+information+in+php/
---

# Aspose.Diagram for Java : Retrieve the Masters Information in PHP


## Aspose.Diagram - Retrieve the Masters Information

To Retrieve the Masters Information using **Aspose.Diagram Java for PHP**, simply invoke **GetMasterInfo** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;
while ($i<sizeof($masters->getCount())){
$master = $masters->get($i);
print "Master ID : " . (string)$master->getID().PHP_EOL;
print "Master Name : " . (string)$master->getName().PHP_EOL;
$i += 1;
}
{{< /code >}}

## Download Running Code

Download **Retrieve the Masters Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)

