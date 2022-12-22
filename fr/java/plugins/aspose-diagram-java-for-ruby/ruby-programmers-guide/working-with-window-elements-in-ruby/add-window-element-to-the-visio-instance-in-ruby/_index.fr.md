---
title: Ajouter un élément de fenêtre à l'instance Visio dans Ruby
type: docs
weight: 20
url: /fr/java/add-window-element-to-the-visio-instance-in-ruby/
---
## **Aspose.Diagram - Ajouter un élément de fenêtre à l'instance Visio**
 Pour ajouter un élément de fenêtre à l'instance Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**AddWindowElement** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# initialize window object

window = Rjb::import('com.aspose.diagram.Window').new

\# set window state

window.setWindowState(Rjb::import('com.aspose.diagram.WindowStateValue').MAXIMIZED)

\# set window height

window.setWindowHeight(500)

\# set window width

window.setWindowWidth(500)

\# set window type

window.setWindowType(Rjb::import('com.aspose.diagram.WindowTypeValue').STENCIL)

\# add window object

diagram.getWindows().add(window)

\# save in any supported format

diagram.save(data_dir + "AddWindowElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added window element to the visio instance."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Ajouter un élément de fenêtre à l'instance Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/addwindowelement.rb)
