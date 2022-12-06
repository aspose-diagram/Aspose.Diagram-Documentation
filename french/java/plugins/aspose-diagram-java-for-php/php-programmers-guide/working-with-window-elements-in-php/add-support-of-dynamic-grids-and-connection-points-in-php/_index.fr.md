---
title: Ajout de la prise en charge des grilles dynamiques et des points de connexion en PHP
type: docs
weight: 10
url: /fr/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram - Ajout de la prise en charge des grilles dynamiques et des points de connexion**
 Pour ajouter la prise en charge des grilles dynamiques et des points de connexion à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**AddDynamicGridsAndConnectionPoints** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# check dynamic grid option

$window->setDynamicGridEnabled(1);

\# check connection points option

$window->setShowConnectionPoints(1);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Ajout de la prise en charge des grilles dynamiques et des points de connexion (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
