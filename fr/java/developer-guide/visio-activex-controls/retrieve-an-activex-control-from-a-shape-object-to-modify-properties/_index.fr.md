---
title: Récupérer un contrôle ActiveX à partir d'un objet de forme pour modifier les propriétés
type: docs
weight: 20
url: /fr/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

À l'aide de Aspose.Diagram API, les développeurs peuvent récupérer un contrôle ActiveX à partir d'un objet de forme Visio pour définir toutes ses propriétés disponibles.

{{% /alert %}} 
## **Récupérer un exemple de programmation de contrôle ActiveX**
[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe propose la méthode getActiveXControl qui permet aux développeurs de récupérer un contrôle ActiveX à partir d'un objet de forme Visio. Les développeurs peuvent caster un contrôle ActiveX dans la classe de contrôle ActiveX appropriée, puis définir toutes ses propriétés disponibles.

```
{{< highlight "java" >}}
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
```
