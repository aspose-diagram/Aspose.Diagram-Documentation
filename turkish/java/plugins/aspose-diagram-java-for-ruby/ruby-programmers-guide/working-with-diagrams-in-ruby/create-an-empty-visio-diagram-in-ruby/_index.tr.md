---
title: Ruby'de boş bir Visio Diagram oluşturun
type: docs
weight: 10
url: /tr/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Boş bir Visio Diagram oluştur**
 Kullanarak boş bir Visio Diagram oluşturmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**Diyagram Oluştur** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Boş bir Visio Diagram (Aspose.Diagram) oluşturun**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
