---
title: Введение
type: docs
weight: 10
url: /ru/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio сохраняет информацию о действиях, предпринятых над diagram в файле. Например, время и дата создания документа, время последнего редактирования, печати или сохранения сохраняются вместе с файлом. Также сохраняется информация о том, какая версия Microsoft Visio создала и последний раз редактировала файл.

В этой статье объясняется, как получить эту информацию.

{{% /alert %}} 
## **Получите версию библиотеки Aspose.Diagram for Java**
 Метод getVersion(), предоставляемый[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) класс и метод getBuildNumberCreated(), предоставляемый[Свойства документа](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class используются для определения версии и полного номера сборки экземпляра Microsoft Visio, используемого для создания документа.
### **Определение версии Microsoft Visio, которая создала, отредактировала и сохранила документ**
 Метод getBuildNumberEdited(), предоставляемый[Свойства документа](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class используется для определения полного номера сборки экземпляра Microsoft Visio, используемого для редактирования документа.

Методы getTimeCreated(), getTimeEdited(), getTimePrinted() и getTimeSaved(), предоставляемые[Свойства документа](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class используются для определения времени создания, последнего редактирования, последней печати и последнего сохранения документа Microsoft Visio.

Вы также можете установить эти свойства, чтобы изменить информацию в файле.

В приведенных ниже примерах кода показано, как получить информацию о том, что создало файл, а также когда он был создан, отредактирован, распечатан и сохранен.

**Вывод кода в окно консоли** 

![дело:изображение_альтернативный_текст](introduction_1.png)
#### **Образец программирования**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetLibraryVersion.class);
// build path of an existing diagram
String path = dataDir + "Drawing1.vsdx";

//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(path);

//Display Visio version and document modification time at different stages
System.out.println("Visio Instance Version : " + diagram.getVersion());
System.out.println("Full Build Number Created : " + diagram.getDocumentProps().getBuildNumberCreated());
System.out.println("Full Build Number Edited : " + diagram.getDocumentProps().getBuildNumberEdited());
System.out.println("Date Created : " + diagram.getDocumentProps().getTimeCreated());
System.out.println("Date Last Edited : " + diagram.getDocumentProps().getTimeEdited());
System.out.println("Date Last Printed : " + diagram.getDocumentProps().getTimePrinted());
System.out.println("Date Last Saved : " + diagram.getDocumentProps().getTimeSaved());

{{< /highlight >}}

## **Письмо Microsoft Visio Сводная информация о документе**
Microsoft Visio позволяет определить ряд свойств сводной информации документа, чтобы помочь вам и вашим коллегам идентифицировать документ diagram. Свойства сводки, например, заголовок, тема, автор и описание, облегчают поиск файла при поиске и распознавание при просмотре. файлы.

[Свойства документа](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)Класс предоставляет ряд свойств для установки или получения сводной информации Microsoft Visio diagram. Aspose.Diagram for Java может обновить сводную информацию о чертеже, а затем записать файл чертежа обратно в VDX.

{{% alert color="primary" %}} 

Обратите внимание, что вы не можете устанавливать значения против**Заявление**а также**Режиссер**поля, потому что Aspose Ltd. и Aspose.Diagram for Java xxx будут отображаться против этих полей.

{{% /alert %}} 
### **Письмо Microsoft Visio Сводная информация о документе**
Чтобы обновить сводную информацию о чертеже существующего файла VDX или VSD:

1.  Создайте экземпляр[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) учебный класс.
1. Задайте свойства, предоставляемые методом Diagram.getDocumentProps(), чтобы определить сводную информацию для файла чертежа Visio.
1. Вызовите метод save() класса Diagram, чтобы записать файл чертежа Visio в VDX.

Проверьте сводную информацию:

1. Откройте выходной файл VDX в Microsoft Visio.
1.  Выбор**Информация** от**Файл** меню.

**Диалоговое окно «Информация», показывающее обновленную сводную информацию** 

![дело:изображение_альтернативный_текст](introduction_2.png)
#### **Образец программирования**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetVisioProperties.class);
// build path of an existing diagram
String path = dataDir + "Drawing1.vsdx";

//Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(path);

//Set some summary information about the diagram
diagram.getDocumentProps().setCreator("Ijaz");
diagram.getDocumentProps().setCompany("Aspose");
diagram.getDocumentProps().setCategory("Drawing 2D");
diagram.getDocumentProps().setManager("Sergey Polshkov");
diagram.getDocumentProps().setTitle("Aspose Title");
diagram.getDocumentProps().setTimeCreated(DateTime.getNow());
diagram.getDocumentProps().setSubject("Visio Diagram");
diagram.getDocumentProps().setTemplate("Aspose Template");

//Write the updated file to the disk in VSDX file format
diagram.save(dataDir + "SetVisioProperties_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Определить формат файла Visio**
 С использованием[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, разработчики могут определить формат файла Visio перед его открытием, поскольку расширение файла не гарантирует, что содержимое файла является соответствующим.
### **Образец программирования определения формата**
В следующем примере кода показано, как определить формат файла (используя путь к файлу или поток) и проверить его расширение.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectVisioFileFormat.class);

		// detect file format using the direct file path
		FileFormatInfo info = FileFormatUtil.detectFileFormat(dataDir + "Drawing1.vsdx");

		// get the detected file format
		System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}

## **Определить формат файла Visio из InputStream**
Используя Aspose.Diagram for Java API, разработчики могут определять формат файла Visio, передавая входной поток. Для этого можно использовать метод detectFileFormat класса FileFormatUtil.
### **Определение формата из примера программирования InputStream**
В следующем примере кода показано, как определить формат файла с помощью входного потока.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}

