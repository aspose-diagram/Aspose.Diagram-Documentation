---
title: Ruby'de Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Gösterme ve Gizleme
type: docs
weight: 40
url: /tr/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Göster ve Gizle**
Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Göstermek ve Gizlemek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**ShowHideProperties** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'in (Aspose.Diagram) Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Gösterme ve Gizleme**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/showhideproperties.rb)
