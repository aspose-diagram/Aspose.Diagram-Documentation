---
title: Ajouter la prise en charge des grilles dynamiques et des points de connexion dans Ruby
type: docs
weight: 10
url: /fr/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/
---
## **Aspose.Diagram - Ajout de la prise en charge des grilles dynamiques et des points de connexion**
 Pour ajouter la prise en charge des grilles dynamiques et des points de connexion à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**AddDynamicGridsAndConnectionPoints** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get window object by index

window = diagram.getWindows().get(0)

\# check dynamic grid option

window.setDynamicGridEnabled(1)

\# check connection points option

window.setShowConnectionPoints(1)

\# Save as VDX

diagram.save(data_dir + "AddDynamicGridsAndConnectionPoints.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)

puts "Added Support of Dynamic Grids and Connection Points in the Visio Drawings."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Ajout de la prise en charge des grilles dynamiques et des points de connexion (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
