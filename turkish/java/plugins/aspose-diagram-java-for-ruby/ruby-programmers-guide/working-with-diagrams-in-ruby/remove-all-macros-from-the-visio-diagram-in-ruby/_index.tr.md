---
title: Ruby'de Visio Diagram'den Tüm Makroları Kaldır
type: docs
weight: 50
url: /tr/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'den Tüm Makroları Kaldır**
 Visio Diagram'den Tüm Makroları Kaldırmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**DiyagramdanTüm Makroları Kaldır** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# remove all macros

diagram.setVbProjectData(nil)

\# Save as VDX

diagram.save(data_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Removed all macros from diagram successfully!"

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'den (Aspose.Diagram) Tüm Makroları Kaldır**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
