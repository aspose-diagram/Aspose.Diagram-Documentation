---
title: Ruby'de Dinamik Izgaralar ve Bağlantı Noktaları Desteği Ekleyin
type: docs
weight: 10
url: /tr/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/
---
## **Aspose.Diagram - Dinamik Şebekeler ve Bağlantı Noktaları Desteği Ekleyin**
 Kullanarak Dinamik Izgaralar ve Bağlantı Noktaları Desteği Eklemek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**DynamicGridsAndConnectionPoints Ekle** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Dinamik Şebekeler ve Bağlantı Noktaları Desteği Ekleyin (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
