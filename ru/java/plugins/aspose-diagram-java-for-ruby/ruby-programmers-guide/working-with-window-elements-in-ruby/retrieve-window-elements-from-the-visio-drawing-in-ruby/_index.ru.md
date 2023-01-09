---
title: Извлечение элементов окна из чертежа Visio в Ruby
type: docs
weight: 30
url: /ru/java/retrieve-window-elements-from-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram — Извлечение оконных элементов из чертежа Visio**
 Извлечение оконных элементов из чертежа Visio с помощью**Aspose.Diagram Java для рубина** , просто вызовите**GetWindowElements** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

окна = diagram.getWindows()

я = 0

 в то время как я< windows.getCount()

    window = windows.get(i)

    puts "ID: " + window.getID().to_s

    puts "Type: " + window.getWindowType().to_s

    puts "Window height: " + window.getWindowHeight().to_s

    puts "Window width: " + window.getWindowWidth().to_s

    puts "Window state: " + window.getWindowState().to_s

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Извлечение оконных элементов из чертежа Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
