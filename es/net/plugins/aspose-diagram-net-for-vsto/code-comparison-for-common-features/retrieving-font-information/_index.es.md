---
title: Recuperación de información de fuentes
type: docs
weight: 80
url: /es/net/retrieving-font-information/
---
## **VSTO**
continuación se muestra el código para recuperar la información de la fuente:

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram dispone de mecanismos de recuperación de información sobre los elementos que componen un diagram, de[paginas](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) , plantillas,[conectores](/diagram/es/net/retrieving-connector-information/) también fuentes. Este artículo muestra cómo averiguar qué fuentes se utilizan en un diagram.

{{% /alert %}} 

 los[Fuente](https://reference.aspose.com/diagram/net/aspose.diagram/font) objeto representa un tipo de letra que se aplica al texto de un documento o que está disponible para su uso en el sistema.

Un objeto Fuente asigna un nombre (por ejemplo, "Arial") al ID de fuente (por ejemplo, 3) que Microsoft Visio almacena en una celda Fuente en una sección Carácter de una forma que contiene texto formateado con esa fuente. Los ID de fuente pueden cambiar cuando se abre un documento en diferentes sistemas o cuando se instalan o eliminan fuentes.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **Descargar código de muestra**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Descargar código de ejecución**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
