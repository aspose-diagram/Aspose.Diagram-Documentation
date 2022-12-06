---
title: Получение информации о шрифте
type: docs
weight: 80
url: /ru/net/retrieving-font-information/
---
## **ВСТО**
Ниже приведен код для получения информации о шрифте:

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram имеет механизмы для получения информации об элементах, составляющих diagram, из[страницы](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) трафареты,[соединители](/diagram/ru/net/retrieving-connector-information/)а также шрифты. В этой статье показано, как узнать, какие шрифты используются в файле diagram.

{{% /alert %}} 

[Шрифт](https://reference.aspose.com/diagram/net/aspose.diagram/font) объект представляет собой шрифт, который либо применяется к тексту в документе, либо доступен для использования в системе.

Объект Font сопоставляет имя (например, «Arial») с идентификатором шрифта (например, 3), который Microsoft Visio хранится в ячейке «Шрифт» в разделе «Символ» фигуры, содержащей текст, отформатированный с помощью этого шрифта. Идентификаторы шрифтов могут меняться при открытии документа в разных системах или при установке или удалении шрифтов.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **Скачать пример кода**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Скачать рабочий код**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
