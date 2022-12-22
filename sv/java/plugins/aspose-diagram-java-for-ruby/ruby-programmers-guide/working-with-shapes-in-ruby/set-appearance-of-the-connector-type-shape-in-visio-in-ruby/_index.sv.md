---
title: Ställ in utseendet på kontakttypsformen i Visio i rubin
type: docs
weight: 100
url: /sv/java/set-appearance-of-the-connector-type-shape-in-visio-in-ruby/
---
## **Aspose.Diagram - Ställ in utseendet på kontakttypsformen i Visio**
 För att ställa in utseendet på kontakttypsformen i Visio med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**SetShapeAppearance** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Ställ in utseendet på kontakttypsformen i Visio (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeappearance.rb)
