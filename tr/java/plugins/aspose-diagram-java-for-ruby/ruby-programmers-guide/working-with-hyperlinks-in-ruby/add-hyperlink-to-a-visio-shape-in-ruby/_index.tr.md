---
title: Ruby'de Visio Şekline Köprü Ekleme
type: docs
weight: 10
url: /tr/java/add-hyperlink-to-a-visio-shape-in-ruby/
---
## **Aspose.Diagram - Köprü Ekle**
 Kullanarak Köprü Eklemek için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ŞekileKöprü Ekle** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Initialize Hyperlink object

hyperlink = Rjb::import('com.aspose.diagram.Hyperlink').new

\# Set address value

hyperlink.getAddress().setValue("http://www.google.com/")

\# Set sub address value

hyperlink.getSubAddress().setValue("Sub address here")

\# Set description value

hyperlink.getDescription().setValue("Description here")

\# Set name

hyperlink.setName("MyHyperLink")

\# Add hyperlink to the shape

diagram.getPages().getPage("Flow 1").getShapes().getShape(1).getHyperlinks().add(hyperlink)

\# Save diagram

diagram.save(data_dir + "Hyperlinks.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added hyperlik to shape successfully!"

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Şekline Köprü Ekleme (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/addhyperlinktoshape.rb)
