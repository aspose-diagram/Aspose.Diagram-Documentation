---
title: Skapa ett tomt Visio Diagram i PHP
type: docs
weight: 20
url: /sv/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - Skapa en tom Visio Diagram**
 För att skapa en tom Visio Diagram med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**Skapa Diagram** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Skapa ett tomt Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
