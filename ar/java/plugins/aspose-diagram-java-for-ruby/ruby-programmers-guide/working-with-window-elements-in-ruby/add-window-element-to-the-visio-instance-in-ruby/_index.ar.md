---
title: أضف عنصر النافذة إلى المثيل Visio في روبي
type: docs
weight: 20
url: /ar/java/add-window-element-to-the-visio-instance-in-ruby/
---
## **Aspose.Diagram - إضافة عنصر نافذة إلى مثيل Visio**
 لإضافة عنصر إطار إلى مثيل Visio باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**AddWindowElement** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **قم بتنزيل كود التشغيل**
 تحميل**إضافة عنصر النافذة إلى المثيل Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/addwindowelement.rb)
