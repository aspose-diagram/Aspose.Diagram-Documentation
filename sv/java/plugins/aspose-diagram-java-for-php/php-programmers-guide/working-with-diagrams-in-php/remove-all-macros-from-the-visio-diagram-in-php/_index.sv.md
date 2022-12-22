---
title: Ta bort alla makron från Visio Diagram i PHP
type: docs
weight: 30
url: /sv/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Ta bort alla makron från Visio Diagram**
 För att ta bort alla makron från Visio Diagram med**Aspose.Diagram Java för PHP** , helt enkelt åberopa**Ta bort alla makron från diagrammet** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Ta bort alla makron från Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
