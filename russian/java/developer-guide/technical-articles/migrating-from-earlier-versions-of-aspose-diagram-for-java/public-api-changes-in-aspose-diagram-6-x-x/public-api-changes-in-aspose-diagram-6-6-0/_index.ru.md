---
title: Общедоступный API Изменения в Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /ru/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 6.3.0 до 6.6.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Добавляет форматы VSDM, VSSM и VSTM в класс LoadFileFormat.**
В этой версии добавлена поддержка чтения форматов Visio с поддержкой макросов.
### **Добавляет форматы VSDM, VSSM и VSTM в класс SaveFileFormat.**
В этой версии добавлена поддержка записи форматов Visio с поддержкой макросов.
### **Изменить код модуля VBA в Visio Diagram**
Мы добавили классы Vba, VbaProject и VbaModule. Эти классы помогают получить контроль над проектом VBA. Используя эту новую версию 6.6.0 или выше, разработчики могут извлекать и изменять код модуля VBA. Пожалуйста, проверьте этот пример кода:

**Java**

{{< highlight "java" >}}

 // загрузить существующий Visio diagram

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = новый Diagram (ввод);

// извлечь проект VBA

VbaProject v = diagram.getVbaProject();

// Перебираем модули и модифицируем код макроса VBA

для (целое я=0;я< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **Добавляет метод getImageData в класс ForeignData**
Он представляет изображение объекта ole в виде массива байтов. Помимо этого, мы также улучшили работу с объектами OLE. Разработчики теперь также могут заменить объект OLE в Visio diagram. Пожалуйста, проверьте этот пример кода:

**Java**

{{< highlight "java" >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
