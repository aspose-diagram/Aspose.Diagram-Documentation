---
title: Ваше первое приложение Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ru/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

В этом разделе для начинающих показано, как разработчики могут создать простое первое приложение (Hello World), используя Aspose.Diagram' simple API. Приложение создает файл Microsoft Visio со словами Hello World на странице.

{{% /alert %}}

### **Создание приложения Hello World**

Чтобы создать приложение Hello World с помощью Aspose.Diagram API:

1. Создайте экземпляр класса Workbook.
1. Применить лицензию:
 1. Если вы приобрели лицензию, то используйте лицензию в своем приложении, чтобы получить доступ к полному функционалу Aspose.Diagram.
 1. Если вы используете ознакомительную версию компонента (если вы используете Aspose.Diagram без лицензии), пропустите этот шаг.
1. Создайте новый файл Microsoft Visio или откройте существующий файл, в который вы хотите добавить/обновить текст.
1.  Вставьте слова**Привет, мир!** на доступную страницу.
1. Создайте измененный файл Microsoft Visio.

Приведенные ниже примеры демонстрируют описанные выше шаги.

#### **Создание Diagram**

В следующем примере создается новый diagram с нуля, пишется слова «Hello World!» на первой странице и сохраняет файл.

**Создайте новый файл visio** 

![дело:изображение_альтернативный_текст](your-first-aspose-diagram-application-hello-world_1.png)

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **Открытие существующего файла**

В следующем примере открывается существующий файл шаблона Microsoft Visio и записываются слова «Hello World!» на первой странице и сохраняет diagram как новый файл.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
