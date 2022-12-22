---
title: Общедоступный API Изменения в Aspose.Diagram 6.6.0
type: docs
weight: 20
url: /ru/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 6.3.0 до 6.6.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Добавляет форматы VSDM, VSSM и VSTM в класс LoadFileFormat.**
В этой версии добавлена поддержка чтения форматов Visio с поддержкой макросов.
## **Добавляет форматы VSDM, VSSM и VSTM в класс SaveFileFormat.**
В этой версии добавлена поддержка записи форматов Visio с поддержкой макросов.
## **Изменить код модуля VBA в Visio Diagram**
Мы добавили классы VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference и VbaProjectReferenceCollection. Эти классы помогают получить контроль над проектом VBA. Используя эту новую версию 6.6.0 или выше, разработчики могут извлекать и изменять код модуля VBA. Пожалуйста, проверьте этот пример кода:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

Ошибка рендеринга макроса 'code': указано недопустимое значение для параметра lang
## **Добавляет свойство ImageData в класс ForeignData.**
Он представляет изображение объекта ole в виде массива байтов. Помимо этого, мы также улучшили работу с объектами OLE. Разработчики теперь также могут заменить объект OLE в Visio diagram. Пожалуйста, проверьте этот пример кода:

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

Ошибка рендеринга макроса 'code': указано недопустимое значение для параметра lang
