---
title: Faire pivoter une forme avec un angle approprié en rubis
type: docs
weight: 80
url: /fr/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - Faire pivoter une forme avec un angle approprié**
 Pour faire pivoter une forme avec un angle approprié à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**RotationForme** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add a shape and set the angle

diagram.getPages().getPage(0).getShapes().getShape(1).setAngle(190)

\# Save diagram

diagram.save(data_dir + "RotateShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Rotated shape."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Faire pivoter une forme avec un angle approprié (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
