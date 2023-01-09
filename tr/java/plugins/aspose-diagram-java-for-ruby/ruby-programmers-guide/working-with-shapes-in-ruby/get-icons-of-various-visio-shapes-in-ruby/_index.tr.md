---
title: Ruby'de Çeşitli Visio Şekillerinin Simgelerini Alın
type: docs
weight: 40
url: /tr/java/get-icons-of-various-visio-shapes-in-ruby/
---
## **Aspose.Diagram - Çeşitli Visio Şekillerinin Simgelerini Alın**
 Kullanarak Çeşitli Visio Şekillerinin Simgelerini Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetShapeIcon** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Basic_Shapes.vsd")

\# get master

master = diagram.getMasters().getMasterByName("Circle")

\# get byte array

bytes = master.getIcon()

\# create an image file

fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "MyImage.png")

\# write byte array of the image

fos.write(bytes)

\# close array

fos.close()

puts "Get shape icon, please check the output file."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Çeşitli Visio Şekillerinin Simgelerini Alın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
