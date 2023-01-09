---
title: إظهار وإخفاء الشبكات والمساطر والأدلة وفواصل الصفحات من Visio Diagram في روبي
type: docs
weight: 40
url: /ar/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - إظهار وإخفاء الشبكات والمساطر والموجهات وفواصل الصفحات لـ Visio Diagram**
لإظهار وإخفاء الشبكات والمساطر والأدلة وفواصل الصفحات من Visio Diagram باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**إظهارإخفاء الخصائص** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **قم بتنزيل كود التشغيل**
 تحميل**إظهار وإخفاء الشبكات والمساطر والأدلة وفواصل الصفحات Visio Diagram (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/showhideproperties.rb)
