---
title: Чтение пользовательских ячеек Shape в Ruby
type: docs
weight: 20
url: /ru/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - Чтение пользовательских ячеек фигуры**
 Чтобы прочитать пользовательские ячейки формы, используя**Aspose.Diagram Java для рубина** , просто вызовите**Реадусердефинедселлс** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

формы = diagram.getPages().getPage("Поток 1").getShapes()

я = 0

 в то время как я< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        users = shape.getUsers()

        j = 0

        while j < users.getCount()

            user = users.get(j)

            puts user.getName() + ": " + user.getValue().getVal()

            j +=1

        end

        break

    end

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Чтение пользовательских ячеек Shape (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
