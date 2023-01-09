---
title: قراءة قيم XML من SolutionXML Element في Ruby
type: docs
weight: 20
url: /ar/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram - قراءة قيم XML من SolutionXML Element**
 لقراءة قيم XML من SolutionXML Element باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**ReadXmlValues** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs ()

أنا = 0

 عندما أنا< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**قراءة قيم XML من SolutionXML Element (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
