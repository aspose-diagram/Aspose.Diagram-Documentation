---
title: Получение информации о соединителе
type: docs
weight: 90
url: /ru/net/retrieving-connector-information/
---
## **ВСТО**
Ниже приведен код для получения информации о соединителе:

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram for .NET предоставляет механизмы для получения информации - ID и имя - о[страницы](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) а также[мастер](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). Он также позволяет получить информацию о соединителях, элементах, которые связывают фигуры.

{{% /alert %}} 

[Соединять](https://reference.aspose.com/diagram/net/aspose.diagram/connect) Объект представляет соединитель, который соединяет две фигуры на странице рисования Visio. Свойство Connects, предоставляемое[Страница](https://reference.aspose.com/diagram/net/aspose.diagram/page) class поддерживает набор объектов Aspose.Diagram.Connect. Это свойство можно использовать для получения сведений об идентификаторе и имени соединителя.

Ниже приведен код для получения информации о соединителе с использованием Aspose.Diagram .NET:

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[1].Connects)

 {

   //Display information about the Connectors

   Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);

   Console.WriteLine("To Shape ID : " + connector.ToSheet);

 }

 Console.ReadLine();


{{< /highlight >}}
## **Скачать пример кода**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Скачать рабочий код**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
