---
title: أضف عنصر SolutionXML إلى رسم Visio بلون الياقوت
type: docs
weight: 10
url: /ar/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - إضافة SolutionXML Element إلى رسم Visio**
 لإضافة عنصر SolutionXML إلى رسم Visio باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**AddSolutionXmlElement** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# initialize SolutionXML object

solution_xml = Rjb::import('com.aspose.diagram.SolutionXML').new

\# set name

solution_xml.setName("Solution XML")

\# set xml value

solution_xml.setXmlValue("XML Value")

\# add SolutionXML element

diagram.getSolutionXMLs().add(solution_xml)

\# save Visio diagram

diagram.save(data_dir + "SolutionXmlElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added SolutionXML Element to the Visio Drawing."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**أضف عنصر SolutionXML إلى رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/addsolutionxmlelement.rb)
