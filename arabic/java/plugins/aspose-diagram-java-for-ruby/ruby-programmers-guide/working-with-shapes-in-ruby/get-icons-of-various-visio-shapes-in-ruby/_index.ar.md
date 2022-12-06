---
title: احصل على أيقونات بأشكال Visio مختلفة في روبي
type: docs
weight: 40
url: /ar/java/get-icons-of-various-visio-shapes-in-ruby/
---
## **Aspose.Diagram - احصل على أيقونات لأشكال Visio مختلفة**
 للحصول على أيقونات لأشكال Visio المختلفة باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetShapeIcon** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **قم بتنزيل كود التشغيل**
 تحميل**الحصول على أيقونات لأشكال Visio مختلفة (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
