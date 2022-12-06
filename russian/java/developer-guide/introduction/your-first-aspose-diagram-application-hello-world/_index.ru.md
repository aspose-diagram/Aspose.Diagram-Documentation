---
title: Ваше первое приложение Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ru/java/your-first-aspose-diagram-application-hello-world/
description: На этой странице описывается, как создать первое приложение с библиотекой Aspose.Diagram.
---
{{% alert color="primary" %}}

В этом руководстве показано, как создать самое первое приложение (Hello World) с помощью простого Aspose.Diagram API. Это простое приложение создает файл Microsoft Visio с текстом «Hello World» на указанной странице.

{{% /alert %}}

## **Создание приложения Hello World**

Следующие шаги создают приложение Hello World, используя Aspose.Diagram API:

1.  Создайте экземпляр[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) учебный класс.
1.  Если у вас есть лицензия, то[применить это](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 Если вы используете ознакомительную версию, пропустите строки кода, связанные с лицензией.
1. Создайте новый файл Visio или откройте существующий файл Visio.
1. Создайте новое текстовое поле.
1.  Вставьте слова**Привет, мир!** в текстовое поле.
1. Создайте измененный файл Microsoft Visio.

Реализация вышеуказанных шагов продемонстрирована на примерах ниже.

### **Пример кода: создание нового Diagram**

В следующем примере создается новый diagram с нуля, пишет Hello World! на первой странице и сохраняет файл Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **Пример кода: открытие существующего файла**

В следующем примере открывается существующий файл шаблона Microsoft Visio с именем «Sample.vsdx», вводится «Hello World!» текст на первой странице и сохраняет diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
