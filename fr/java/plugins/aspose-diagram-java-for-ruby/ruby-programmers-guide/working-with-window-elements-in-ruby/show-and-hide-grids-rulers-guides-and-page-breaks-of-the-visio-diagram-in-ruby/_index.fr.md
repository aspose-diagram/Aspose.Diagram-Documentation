---
title: Afficher et masquer les grilles, les règles, les guides et les sauts de page du Visio Diagram en Ruby
type: docs
weight: 40
url: /fr/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Afficher et masquer les grilles, les règles, les guides et les sauts de page du Visio Diagram**
Pour afficher et masquer les grilles, les règles, les guides et les sauts de page du Visio Diagram à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**AfficherMasquerPropriétés** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get window object by index

window = diagram.getWindows().get(0)

\# set visibility of grid

window.setShowGrid(1)

\# set visibility of guides

window.setShowGuides(1)

\# set visibility of rulers

window.setShowRulers(1)

\# set visibility of page breaks

window.setShowPageBreaks(1)

\# save in any supported format

diagram.save(data_dir + "ShowHideProperties.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Afficher et masquer les grilles, les règles, les guides et les sauts de page du Visio Diagram (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/showhideproperties.rb)
