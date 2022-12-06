---
title: Извлечение пользовательских ячеек из таблицы форм в Ruby
type: docs
weight: 30
url: /ru/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---
## **Aspose.Diagram - Извлечение пользовательских ячеек из таблицы форм**
 Чтобы получить пользовательские ячейки из Shapesheet, используя**Aspose.Diagram Java для рубина** , просто вызовите**GetUserDefinedCells** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

страницы = diagram.getPages()

количество = 0

 пока считай< pages.getCount()

    page = pages.get(count)

    shapes = page.getShapes()

    i = 0

    while i < shapes.getCount()

        shape = shapes.get(i)

        if shape.getNameU() == "Process"

            users = shape.getUsers()

            j = 0

            while j < users.getCount()

                user = users.get(j)

                            puts "Name: " + user.getNameU() + " Value: " + user.getValue().getVal() + " Prompt: " + user.getPrompt().getValue()

                j +=1

            end

            break

        end

        i +=1

    end

    count +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Извлечение пользовательских ячеек из таблицы форм (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
