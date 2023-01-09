---
title: Вставьте новую пустую страницу в рисунок Visio в Ruby
type: docs
weight: 20
url: /ru/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram — вставить новую пустую страницу в чертеж Visio**
 Чтобы вставить новую пустую страницу в чертеж Visio с помощью**Aspose.Diagram Java для рубина** , просто вызовите**Добавить страницу** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 деф инициализировать ()

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

 Вызвать конструктор diagram для загрузки diagram из файла VSD

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 # Получить максимальный идентификатор страницы

 Максимум_страница_идентификатор = получить_Максимум_page_id (diagram)

 # Инициализировать новый объект страницы

 new_page = Rjb::import('com.aspose.diagram.Page').новый

 # Имя набора

 new_page.setName("новая страница")



 # Установить идентификатор страницы

 новый_page.setID (макс._page_id + 1)

 # Или попробуйте конструктор страниц

 # Страница newPage = новая страница (MaxPageId + 1);

 # Добавляем новую пустую страницу

 diagram.getPages().добавить(новая_страница)

 # Сохранить diagram

 diagram.сохранить(данные_директор + "Новая страница_Output.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

 ставит "Добавлена новая страница".

конец

деф получить_Максимум_page_id (diagram)

макс = diagram.getPages().getPage(0).getID()

 я = 1

 в то время как я< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Вставка новой пустой страницы в чертеж Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
