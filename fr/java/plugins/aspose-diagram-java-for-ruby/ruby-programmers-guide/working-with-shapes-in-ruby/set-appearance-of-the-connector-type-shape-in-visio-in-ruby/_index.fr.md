---
title: Définir l'apparence de la forme du type de connecteur dans Visio en rubis
type: docs
weight: 100
url: /fr/java/set-appearance-of-the-connector-type-shape-in-visio-in-ruby/
---
## **Aspose.Diagram - Définir l'apparence de la forme du type de connecteur dans Visio**
 Pour définir l'apparence de la forme du type de connecteur dans Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**DéfinirApparenceForme** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set dynamic connector appearance

shape.setConnectorsType(Rjb::import('com.aspose.diagram.ConnectorsTypeValue').STRAIGHT_LINES)

\# Save diagram

diagram.save(data_dir + "SetShapeAppearance.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set appearnce of the connector type shape."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Définir l'apparence de la forme du type de connecteur dans Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeappearance.rb)
