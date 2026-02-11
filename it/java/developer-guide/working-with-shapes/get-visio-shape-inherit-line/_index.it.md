---
title: Ottieni Visio Shape Eredita linea
type: docs
weight: 100
url: /it/java/get-visio-shape-inherit-line/
description: Questa sezione spiega come ottenere lo stile di linea della forma visio ereditato dal suo stile genitore e master con Aspose.Diagram.
---
### **Recupera dati linea ereditati di una forma Visio**
 Le forme Visio possono ereditare lo stile padre e la forma master. Gli sviluppatori possono ottenere o impostare i dati della linea ereditata di una forma Visio. La proprietà InheritLine, esposta da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, contiene i valori di formattazione della linea per la forma ereditata dallo stile genitore e dalla forma principale.
#### **Recupera esempio di programmazione dei dati della riga ereditata**
Il frammento di codice seguente recupera i dati della linea ereditati della forma. Si prega di controllare questo codice di esempio:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}


