---
title: Показать и скрыть сетки, линейки, направляющие и разрывы страниц Visio Diagram в Ruby
type: docs
weight: 40
url: /ru/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram — Показать и скрыть сетки, линейки, направляющие и разрывы страниц Visio Diagram**
Чтобы показать и скрыть сетки, линейки, направляющие и разрывы страниц Visio Diagram с помощью**Aspose.Diagram Java для рубина** , просто вызовите**ПоказатьСкрытьСвойства** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

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
## **Скачать рабочий код**
 Скачать**Показать и скрыть сетки, линейки, направляющие и разрывы страниц Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/showhideproperties.rb)
