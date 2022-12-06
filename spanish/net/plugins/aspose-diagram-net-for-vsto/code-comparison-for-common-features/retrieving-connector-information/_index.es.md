---
title: Recuperación de información del conector
type: docs
weight: 90
url: /es/net/retrieving-connector-information/
---
## **VSTO**
A continuación se muestra el código para obtener información del conector:

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram for .NET proporciona mecanismos para la recuperación de información - DNI y nombre - sobre[paginas](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) y[Maestro](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). También te permite obtener información sobre los conectores, los elementos que unen las formas.

{{% /alert %}} 

 los[Conectar](https://reference.aspose.com/diagram/net/aspose.diagram/connect) El objeto representa un conector que une dos formas en una página de dibujo Visio. La propiedad Conecta, expuesta por el[Página](https://reference.aspose.com/diagram/net/aspose.diagram/page) La clase admite una colección de objetos Aspose.Diagram.Connect. Esta propiedad se puede utilizar para recuperar información de ID y nombre sobre un conector.

A continuación se muestra el código para obtener información del conector usando Aspose.Diagram .NET:

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
## **Descargar código de muestra**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Descargar código de ejecución**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
