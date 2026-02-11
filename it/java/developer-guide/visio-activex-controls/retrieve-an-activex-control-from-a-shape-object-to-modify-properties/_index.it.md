---
title: Recuperare un controllo ActiveX da un oggetto Shape per modificare le proprietà
type: docs
weight: 20
url: /it/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

Utilizzando Aspose.Diagram API, gli sviluppatori possono recuperare un controllo ActiveX da un oggetto forma Visio per impostarne tutte le proprietà disponibili.

{{% /alert %}} 
## **Recupera un esempio di programmazione di controlli ActiveX**
[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) offre il metodo getActiveXControl che consente agli sviluppatori di recuperare un controllo ActiveX da un oggetto shape Visio. Gli sviluppatori possono eseguire il cast di un controllo ActiveX nella classe di controllo ActiveX appropriata e quindi impostarne tutte le proprietà disponibili.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveActiveXControl.class) + "VisioActiveXControls/";
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// get a Visio page by name
Page page = diagram.getPages().getPage("Page-1");
// get a shape by ID
Shape shape = page.getShapes().getShape(1);
// get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();
// set width of the command button control
cbac.setWidth(4);
// set height of the command button control
cbac.setHeight(4);
// set caption of the command button control
cbac.setCaption("Test Button");
// save diagram
diagram.save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

