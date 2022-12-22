---
title: Ruby'de Visio Çizimlere Yorum Ekleyin
type: docs
weight: 40
url: /tr/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - Visio Çizimlerine Yorum Ekle**
 Visio Çizimine Yorum Eklemek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**DiyagramaYorum Ekle** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add comment

diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

\# Save as VDX

diagram.save(data_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added comment successfully!"

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çizimlere Yorum Ekle (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
