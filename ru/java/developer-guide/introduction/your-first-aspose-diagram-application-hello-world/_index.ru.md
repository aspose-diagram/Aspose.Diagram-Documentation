---
title: Ваша первая заявка Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ru/java/your-first-aspose-diagram-application-hello-world/
description: На этой странице описывается, как создать первое приложение с библиотекой Aspose.Diagram.
---
{{% alert color="primary" %}}

В этом руководстве показано, как создать самое первое приложение (Hello World), используя Aspose.Diagram' simple API. Это простое приложение создает файл Microsoft Visio с текстом 'Hello World' на указанной странице.

{{% /alert %}}

## **Создание приложения Hello World**

Следующие шаги создают приложение Hello World, используя Aspose.Diagram API:

1.  Создайте экземпляр[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) учебный класс.
1.  Если у вас есть лицензия, то[применить это](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 Если вы используете ознакомительную версию, пропустите строки кода, связанные с лицензией.
1. Создайте новый файл Visio или откройте существующий файл Visio.
1. Создайте новое текстовое поле.
1.  Вставьте слова**Hello World!** в текстовое поле.
1. Создайте измененный файл Microsoft Visio.

Реализация вышеуказанных шагов продемонстрирована на примерах ниже.

### **Пример кода: создание нового Diagram**

В следующем примере создается новый diagram с нуля, пишет Hello World! на первой странице и сохраняет файл Visio.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


### **Пример кода: открытие существующего файла**

В следующем примере открывается существующий файл шаблона Microsoft Visio с именем «Sample.vsdx», вводится «Hello World!» текст на первой странице и сохраняет diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadVisioDiagram.class);   
// Open the stream. Read only access is enough for Aspose.Diagram to load a diagram.
InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

//Call the diagram constructor to load diagram from a VSDX stream
Diagram vsdDiagram = new Diagram(stream);
stream.close();

//Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load diagram from a VSS file
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}

