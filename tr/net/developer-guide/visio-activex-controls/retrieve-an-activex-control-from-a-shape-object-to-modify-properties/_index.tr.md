---
title: Özellikleri Değiştirmek için Şekil Nesnesinden ActiveX Denetimi Alın
type: docs
weight: 20
url: /tr/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Aspose.Diagram kitaplığıyla bir activeX Denetiminin özelliklerini değiştirin.
---
{{% alert color="primary" %}} 

Geliştiriciler, Aspose.Diagram API'i kullanarak, mevcut tüm özelliklerini ayarlamak için bir Visio şekil nesnesinden bir ActiveX denetimi alabilir.

{{% /alert %}} 
## **Bir ActiveX Kontrol Programlama Örneği Alın**
[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, geliştiricilerin bir Visio şekil nesnesinden bir ActiveX denetimi almasına izin veren ActiveXControl özelliğini sunar. Geliştiriciler, bir ActiveX denetimini uygun ActiveX denetim sınıfında yayınlayabilir ve ardından tüm kullanılabilir özelliklerini ayarlayabilir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Load and get a Visio page by name
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");            
Page page = diagram.Pages.GetPage("Page-1");
// Get a shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;
// Set width, height and caption of the command button control
cbac.Width = 4;           
cbac.Height = 4;           
cbac.Caption = "Test Button";
// Save diagram
diagram.Save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
