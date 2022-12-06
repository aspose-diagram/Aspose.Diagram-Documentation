---
title: Введение
type: docs
weight: 10
url: /ru/net/introduction/
description: Внедрение библиотеки Aspose.Diagram.
---
## **Получите информацию о документе Visio библиотеки Aspose.Diagram for .NET**
Microsoft Visio сохраняет информацию о действиях, предпринятых над diagram в файле. Например, время и дата создания документа, время последнего редактирования, печати или сохранения сохраняются вместе с файлом. Также сохраняется информация о том, какая версия Microsoft Visio создала и последний раз редактировала файл.

В этой статье объясняется, как получить эту информацию.
### **Определение версии Microsoft Visio, которая создала, отредактировала и сохранила документ**
 Свойство Version, предоставляемое[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)класс, а свойство BuildNumberCreated, предоставляемое классом DocumentProperties, используется для определения версии и полного номера сборки экземпляра Microsoft Visio, используемого для создания документа.

 Свойство BuildNumberEdited, предоставляемое[Свойства документа](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) class используется для определения полного номера сборки экземпляра Microsoft Visio, используемого для редактирования документа.

Свойства TimeCreated, TimeEdited, TimePrinted и TimeSaved, предоставляемые классом DocumentProperties, используются для определения времени создания, последнего редактирования, последней печати и последнего сохранения документа.

Вы также можете установить эти свойства, чтобы изменить информацию в файле. В приведенных ниже примерах кода показано, как получить информацию о том, что создало файл, а также когда он был создан, отредактирован, распечатан и сохранен.
#### **Образец программирования**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Письмо Visio Сводная информация о документе**
Microsoft Visio позволяет определить ряд свойств сводной информации документа, чтобы помочь вам и вашим коллегам идентифицировать diagram. просмотр файлов.
### **Письмо Microsoft Visio Сводная информация о документе**
Класс DocumentProperties предоставляет ряд свойств для установки или получения сводной информации Microsoft Visio diagram. Aspose.Diagram for .NET может обновить сводную информацию о чертеже, а затем записать файл чертежа обратно в VDX.

{{% alert color="primary" %}} 

Обратите внимание, что вы не можете устанавливать значения против**Заявление**а также**Режиссер**поля, потому что Aspose Ltd. и Aspose.Diagram for .NET xxx будут отображаться против этих полей.

{{% /alert %}} 

Чтобы обновить сводную информацию о чертеже существующего файла VDX или VSD:

1.  Создайте экземпляр[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) учебный класс.
1.  Установить свойства, предоставляемые[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) для определения сводной информации для файла чертежа Visio.
1. Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VDX.

Проверьте сводную информацию:

1. Откройте выходной файл VDX в Microsoft Visio.
1. Выбор Информация из меню Файл.
#### **Написание Visio Сводная информация о документе Образец программирования**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Определить формат файла Visio**
Используя Aspose.Diagram for .NET API, разработчики могут определить формат файла Visio перед его открытием, поскольку расширение файла не гарантирует, что содержимое файла соответствует требованиям.
### **Образец программирования определения формата**
В следующем примере кода показано, как определить формат файла (используя путь к файлу или поток) и проверить его расширение.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
