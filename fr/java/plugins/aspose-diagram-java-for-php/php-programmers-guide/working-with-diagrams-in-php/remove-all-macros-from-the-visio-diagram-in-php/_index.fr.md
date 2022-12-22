---
title: Supprimer toutes les macros du Visio Diagram en PHP
type: docs
weight: 30
url: /fr/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Supprimer toutes les macros du Visio Diagram**
 Pour supprimer toutes les macros du Visio Diagram à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**RemoveAllMacrosFromDiagram** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Supprimer toutes les macros du Visio Diagram (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
