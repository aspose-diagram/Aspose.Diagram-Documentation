---
title: Ruby'de Diyagramları Koruma ve Korumayı Kaldırma
type: docs
weight: 20
url: /tr/java/protect-and-unprotect-diagrams-in-ruby/
---
## **Aspose.Diagram - Diyagramları Koru ve Korumayı Kaldır**
 kullanarak Diyagramları Korumak ve Korumayı Kaldırmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**Korumayı Kaldırma Diyagramı** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

diagram.getDocumentSettings().setProtectBkgnds(1)

diagram.getDocumentSettings().setProtectMasters(1)

diagram.getDocumentSettings().setProtectShapes(1)

diagram.getDocumentSettings().setProtectStyles(1)

\# Save diagram

diagram.save(data_dir + "ProtectUnprotectDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied protection on diagram successfully!"

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Diyagramları Koru ve Korumayı Kaldır (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectdiagram.rb)
