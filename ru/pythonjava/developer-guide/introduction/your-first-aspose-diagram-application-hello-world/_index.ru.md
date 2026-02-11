---
title: Ваша первая заявка Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ru/python-java/your-first-aspose-diagram-application-hello-world/
description: На этой странице описывается, как создать первое приложение с библиотекой Aspose.Diagram.
---
{{% alert color="primary" %}}

В этом руководстве показано, как создать самое первое приложение (Hello World), используя Aspose.Diagram' simple API. Это простое приложение создает файл Microsoft Visio с текстом 'Hello World' на указанной странице.

{{% /alert %}}

## **Создание приложения Hello World**

Следующие шаги создают приложение Hello World, используя Aspose.Diagram API:

1. Создайте экземпляр класса Diagram.
1. Применить лицензию:
 1. Если вы приобрели лицензию, то используйте лицензию в своем приложении, чтобы получить доступ к полному функционалу Aspose.Diagram.
 1. Если вы используете ознакомительную версию компонента (если вы используете Aspose.Diagram без лицензии), пропустите этот шаг.
1. Создайте новый файл Visio или откройте существующий файл Visio.
1. Создайте новое текстовое поле.
1.  Вставьте слова**Hello World!** в текстовое поле.
1. Создайте измененный файл Microsoft Visio.

Реализация вышеуказанных шагов продемонстрирована на примерах ниже.

### **Пример кода: создание нового Diagram и запись Hello World!**

В следующем примере открывается существующий файл шаблона Microsoft Visio с именем "[Basic_Shapes.vss](Basic_Shapes.vss)", вводит текст "Hello World!" на первой странице и сохраняет diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Basic_Shapes.vss")

# Add a new hello world rectangle shape
shapeId = diagram.addShape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.getPages().getPage(0).getShapes().getShape(shapeId)
shape.getText().getValue().add(Txt("Hello World"))

# Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

