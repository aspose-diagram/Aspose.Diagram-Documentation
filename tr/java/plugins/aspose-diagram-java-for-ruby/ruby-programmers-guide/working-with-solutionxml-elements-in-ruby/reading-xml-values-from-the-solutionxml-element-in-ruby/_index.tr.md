---
title: Ruby'deki SolutionXML Öğesinden XML Değerlerini Okuma
type: docs
weight: 20
url: /tr/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram - SolutionXML Öğesinden XML Değerlerini Okuma**
 SolutionXML Öğesinden XML Değerlerini Okumak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ReadXmlValues** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

solution_xmls = diagram.getSolutionXMLs()

ben = 0

 ben iken< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**SolutionXML Öğesinden XML Değerlerini Okuma (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
