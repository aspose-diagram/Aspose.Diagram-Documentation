---
title: Ваша первая заявка Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ru/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

В этом разделе для начинающих показано, как разработчики могут создать простое первое приложение (Hello World), используя Aspose.Diagram' simple API. Приложение создает файл Microsoft Visio со словами Hello World на странице.

{{% /alert %}}

### **Создание приложения Hello World**

Чтобы создать приложение Hello World, используя Aspose.Diagram API:

1. Создайте экземпляр класса Workbook.
1. Применить лицензию:
 1. Если вы приобрели лицензию, то используйте лицензию в своем приложении, чтобы получить доступ к полному функционалу Aspose.Diagram.
 1. Если вы используете ознакомительную версию компонента (если вы используете Aspose.Diagram без лицензии), пропустите этот шаг.
1. Создайте новый файл Microsoft Visio или откройте существующий файл, в который вы хотите добавить/обновить текст.
1.  Вставьте слова**Hello World!** на доступную страницу.
1. Создайте измененный файл Microsoft Visio.

Приведенные ниже примеры демонстрируют описанные выше шаги.

#### **Создание Diagram**

В следующем примере создается новый diagram с нуля, записываются слова «Hello World!» на первой странице и сохраняет файл.

**Создайте новый файл visio** 

![дело:изображение_альтернативный_текст](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **Открытие существующего файла**

В следующем примере открывается существующий файл шаблона Microsoft Visio, записываются слова «Hello World!» на первой странице и сохраняет diagram как новый файл.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

diagram = Diagram(os.path.join(sourceDir, "Basic Shapes.vss"))

#// Add a new hello world rectangle shape
shapeId = diagram.add_shape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.pages[0].shapes.get_shape(shapeId)
shape.text.value.add(Txt("Hello World"))

#// Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}

