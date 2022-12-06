---
title: Управление свойствами документа
linktitle: Свойства документа
type: docs
weight: 80
url: /ru/net/document-properties/
aliases: [/net/document-properties/]
description: Управление свойствами документа visio файлов.
---
## **Введение**

Microsoft Visio предоставляет возможность добавлять свойства к visio файлам. Эти свойства документа предоставляют полезную информацию и разделены на 2 категории, как подробно описано ниже.

- Системные (встроенные) свойства. Встроенные свойства содержат общую информацию о документе, такую как название документа, имя автора, статистику документа и т. д.
- Пользовательские (настраиваемые) свойства: настраиваемые свойства, определенные конечным пользователем в виде пары "имя-значение".

{{% alert color="primary" %}}

Самое важное, что нужно знать о встроенных и настраиваемых свойствах, это то, что к встроенным свойствам можно получить доступ и изменить их, но нельзя создать или удалить. Однако можно создавать настраиваемые свойства и управлять ими.

{{% /alert %}}

## **Управление свойствами документа с помощью Microsoft Visio**

 Microsoft Visio позволяет управлять свойствами документов файлов Visio в режиме WYSIWYG. Пожалуйста, выполните следующие шаги, чтобы открыть**Характеристики** диалог в Visio 2016.

1.  От**Файл** меню, выберите**Информация**.

|**Выбор информационного меню**|
|:- |
|![дело:изображение_альтернативный_текст](managing-document-properties_1.png)|
1.  Нажмите на**Характеристики** заголовок и выберите «Дополнительные свойства».

|**Щелкнув Выбор дополнительных свойств**|
|:- |
|![дело:изображение_альтернативный_текст](managing-document-properties_2.png)|
1. Управление свойствами документа файла.

|**Диалог свойств**|
|:- |
|![дело:изображение_альтернативный_текст](managing-document-properties_3.png)|
В диалоговом окне «Свойства» есть различные вкладки, такие как «Общие», «Сводка», «Статистика», «Содержание» и «Пользовательские настройки». Каждая вкладка помогает настроить различные виды информации, связанной с файлом. Вкладка Custom используется для управления пользовательскими свойствами.

## **Работа со свойствами документа с помощью Aspose.Diagram**

Разработчики могут динамически управлять свойствами документа с помощью API Aspose.Diagram. Эта функция помогает разработчикам хранить полезную информацию вместе с файлом, например, когда файл был получен, обработан, с отметкой времени и т. д.

{{% alert color="primary" %}}

Aspose.Diagram for .NET непосредственно записывает информацию о API и номере версии в выходных документах.

Обратите внимание, что вы не можете поручить Aspose.Diagram for .NET изменить или удалить эту информацию из выходных документов.

{{% /alert %}}

### **Доступ к свойствам документа**

 Aspose.Diagram API поддерживают оба типа свойств документа, встроенные и настраиваемые. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) class представляет файл Visio и, как и файл visio,[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) класс может содержать несколько страниц, каждая из которых представлена[**Страница**](https://reference.aspose.com/diagram/net/aspose.diagram/page) класс, тогда как коллекция страниц представлена[**Коллекция страниц**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)учебный класс.

 Использовать[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram)для доступа к свойствам документа файла, как описано ниже.

- Чтобы получить доступ к встроенным свойствам документа, используйте[**diagram.DocumentProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties).
-  Чтобы получить доступ к пользовательским свойствам документа, используйте[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties/properties/customprops).

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AccessingDocumentProperties.cs" >}}

### **Добавление или удаление пользовательских свойств документа**

Как мы описали ранее в начале этого раздела, разработчики не могут добавлять или удалять встроенные свойства, поскольку эти свойства определяются системой, но можно добавлять или удалять настраиваемые свойства, поскольку они определяются пользователем.

### **Добавление пользовательских свойств**

 Aspose.Diagram API-интерфейсы раскрыли[**Добавлять**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/add) метод для[**CustomPropCollection**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection)класс для добавления настраиваемых свойств в коллекцию.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AddingCustomProperties.cs" >}}

### **Удаление пользовательских свойств**

 Чтобы удалить пользовательские свойства с помощью Aspose.Diagram, вызовите[**CustomPropCollection. Удалить**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/remove)и передайте имя удаляемого свойства документа.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemovingCustomProperties.cs" >}}
