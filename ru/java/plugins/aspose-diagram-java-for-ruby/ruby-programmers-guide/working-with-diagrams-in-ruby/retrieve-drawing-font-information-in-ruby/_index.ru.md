---
title: Получить информацию о шрифте чертежа в Ruby
type: docs
weight: 30
url: /ru/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - Получить информацию о шрифте чертежа**
 Чтобы получить информацию о шрифте чертежа с помощью**Aspose.Diagram Java для рубина** , просто вызовите**GetDiagramFontInfo** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

шрифты = diagram.getFonts()

я = 0

 в то время как я< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о шрифте чертежа (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
