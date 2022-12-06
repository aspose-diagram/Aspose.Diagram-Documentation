---
title: Créez un Visio Diagram vide en PHP
type: docs
weight: 20
url: /fr/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - Créer un Visio Diagram vide**
 Pour créer un Visio Diagram vide en utilisant**Aspose.Diagram Java pour PHP** , invoquez simplement**Créer un diagramme** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Créez un Visio Diagram (Aspose.Diagram) vide**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
