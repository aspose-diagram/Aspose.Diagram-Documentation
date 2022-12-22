---
title: Защита и снятие защиты диаграмм в Ruby
type: docs
weight: 20
url: /ru/java/protect-and-unprotect-diagrams-in-ruby/
---
## **Aspose.Diagram - Диаграммы защиты и снятия защиты**
 Чтобы защитить и снять защиту диаграмм с помощью**Aspose.Diagram Java для рубина** , просто вызовите**ЗащититьСнять защитуДиаграмма** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

diagram.getDocumentSettings().setProtectBkgnds(1)

diagram.getDocumentSettings().setProtectMasters(1)

diagram.getDocumentSettings().setProtectShapes(1)

diagram.getDocumentSettings().setProtectStyles(1)

\# Save diagram

diagram.save(data_dir + "ProtectUnprotectDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied protection on diagram successfully!"

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Защита и снятие защиты диаграмм (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectdiagram.rb)
