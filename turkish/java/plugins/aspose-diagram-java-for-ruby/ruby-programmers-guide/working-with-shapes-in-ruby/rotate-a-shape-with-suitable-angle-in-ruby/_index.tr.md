---
title: Ruby'de Bir Şekli Uygun Açıyla Döndürün
type: docs
weight: 80
url: /tr/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - Bir Şekli Uygun Açıyla Döndür**
 Kullanarak Bir Şekli Uygun Açıyla Döndürmek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Şekli Döndür** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add a shape and set the angle

diagram.getPages().getPage(0).getShapes().getShape(1).setAngle(190)

\# Save diagram

diagram.save(data_dir + "RotateShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Rotated shape."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Şekli Uygun Açıyla Döndürün (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
