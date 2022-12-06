---
title: Получить информацию о мастерах в Ruby
type: docs
weight: 30
url: /ru/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - Получить информацию о мастерах**
 Чтобы получить информацию о мастерах, используя**Aspose.Diagram Java для рубина** , просто вызовите**GetMasterInfo** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Вызвать конструктор diagram для загрузки diagram из файла VSD

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

мастера = diagram.getMasters()

я = 0

 в то время как я< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о мастерах (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
