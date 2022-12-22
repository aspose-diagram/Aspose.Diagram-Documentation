---
title: Написание резюме документа
type: docs
weight: 70
url: /ru/net/writing-document-summary/
---
## **ВСТО**
Ниже приведен код для написания резюме документа Visio:

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio позволяет определить ряд свойств сводной информации документа, чтобы помочь вам и вашим коллегам идентифицировать документ diagram. Свойства сводки, например, заголовок, тема, автор и описание, облегчают поиск файла при поиске и распознавание при просмотре. файлы.

{{% /alert %}} 
### **Письмо Microsoft Visio Сводная информация о документе**
[Свойства документа](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)Класс предоставляет ряд свойств для установки или получения сводной информации Microsoft Visio diagram. Aspose.Diagram for .NET может обновить сводную информацию о чертеже, а затем записать файл чертежа обратно в VDX.

Чтобы обновить сводную информацию о чертеже существующего файла VDX или VSD:

1.  Создайте экземпляр[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) учебный класс.
1. Задайте свойства, предоставляемые Diagram.DocumentProps, чтобы определить сводную информацию для файла чертежа Visio.
1. Вызовите метод Save класса Diagram, чтобы записать файл чертежа Visio в VDX.

Проверьте сводную информацию:

1. Откройте выходной файл VDX в Microsoft Visio.
1.  Выбор**Информация** от**Файл** меню.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Скачать пример кода**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Скачать рабочий код**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
