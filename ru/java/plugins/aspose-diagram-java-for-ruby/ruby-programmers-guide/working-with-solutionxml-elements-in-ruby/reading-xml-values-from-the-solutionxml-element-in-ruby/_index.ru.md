---
title: Чтение значений XML из элемента SolutionXML в Ruby
type: docs
weight: 20
url: /ru/java/reading-xml-values-from-the-solutionxml-element-in-ruby/
---
## **Aspose.Diagram — Чтение значений XML из элемента SolutionXML**
 Чтение значений XML из элемента SolutionXML с помощью**Aspose.Diagram Java для рубина** , просто вызовите**Реадксмлвалуерес** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "SolutionXmlElement.vdx")

решение_xmls = diagram.getSolutionXMLs()

я = 0

 в то время как я< solution_xmls.getCount()

    solution_xml = solution_xmls.get(i)

    # get name property

    puts "Name: " + solution_xml.getName().to_s

    # get xml value

    puts "Value:" + solution_xml.getXmlValue().to_s

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Чтение значений XML из элемента SolutionXML (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/SolutionXML/readxmlvalues.rb)
