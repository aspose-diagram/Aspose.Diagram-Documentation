---
title: Управление кодами VBA Visio с поддержкой макросов diagram.
linktitle: Diagram Проект VBA
type: docs
weight: 200
url: /ru/net/working-with-vbaproject/
description: Добавьте модуль VBA и измените VBA или макрос с помощью библиотеки Aspose.Diagram.
---
## **Добавить модуль VBA**
{{% alert color="primary" %}}

 Aspose.Diagram позволяет добавить новый модуль VBA и код макроса с помощью Aspose.Diagram. Пожалуйста, используйте[**Diagram.VbaProject.Modules.Добавить()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) метод добавления нового модуля VBA внутри diagram

{{% /alert %}}

 Следующий пример кода добавляет новый модуль VBA и код макроса и сохраняет выходные данные в формате VSDM. Один раз вы откроете выходной файл VSDM в Microsoft Visio и щелкните значок**Разработчик > Visual Basic** команд меню, вы увидите модуль с именем «TestModule», а внутри него вы увидите следующий код макроса.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Вот пример кода для создания выходного файла VSDM с модулем VBA и кодом макроса.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.VbaProject.Modules.Add(VbaModuleType.Procedural, "TestModule");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[index];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## **Изменить VBA или макрос**

{{% alert color="primary" %}} 

Вы можете изменить код VBA или макроса, используя Aspose.Diagram. Aspose.Diagram добавил следующее пространство имен и классы для чтения и изменения проекта VBA в файле Visio.

- Aspose.Diagram.Vba
- VbaProject
- ВбаМодулеКоллекция
- VbaModule

Эта статья покажет вам, как изменить код VBA или макроса внутри исходного файла Visio, используя Aspose.Diagram.

{{% /alert %}} 

Следующий пример кода загружает исходный файл Visio, внутри которого находится следующий код VBA или макроса.

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

После выполнения образца кода Aspose.Diagram код VBA или макроса будет изменен следующим образом.

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 Вы можете скачать[исходный файл Visio]() и[выходной файл Visio]() по указанным ссылкам.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[2];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## **Предварительные темы**
- [Проверьте, подписан ли код VBA](/diagram/ru/net/check-if-vba-code-is-signed/)
