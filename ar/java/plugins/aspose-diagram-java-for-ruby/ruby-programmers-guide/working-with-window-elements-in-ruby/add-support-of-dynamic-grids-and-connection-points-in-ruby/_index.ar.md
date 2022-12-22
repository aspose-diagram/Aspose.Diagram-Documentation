---
title: أضف دعمًا للشبكات الديناميكية ونقاط الاتصال في Ruby
type: docs
weight: 10
url: /ar/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/
---
## **Aspose.Diagram - إضافة دعم للشبكات الديناميكية ونقاط الاتصال**
 لإضافة دعم للشبكات الديناميكية ونقاط الاتصال باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**AddDynamicGridsAndConnectionPoints** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **قم بتنزيل كود التشغيل**
 تحميل**إضافة دعم للشبكات الديناميكية ونقاط الاتصال (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
