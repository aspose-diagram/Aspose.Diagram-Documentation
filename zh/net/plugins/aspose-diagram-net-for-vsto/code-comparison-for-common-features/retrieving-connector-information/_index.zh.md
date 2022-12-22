---
title: 检索连接器信息
type: docs
weight: 90
url: /zh/net/retrieving-connector-information/
---
## **VSTO**
下面是获取连接器信息的代码：

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Aspose.Diagram for .NET 提供检索信息的机制 - ID 和名称 - 关于[页数](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)和[掌握](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection).它还可以让您获得有关连接器（连接形状的元素）的信息。

{{% /alert %}} 

这[连接](https://reference.aspose.com/diagram/net/aspose.diagram/connect)对象表示连接 Visio 绘图页上两个形状的连接器。 Connects 属性，由[页](https://reference.aspose.com/diagram/net/aspose.diagram/page)类支持 Aspose.Diagram.Connect 对象的集合。此属性可用于检索有关连接器的 ID 和名称信息。

下面是使用Aspose.Diagram .NET获取连接器信息的代码：

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
## **下载示例代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **下载运行代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
