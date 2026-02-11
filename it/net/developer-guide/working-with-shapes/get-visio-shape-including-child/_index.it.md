---
title: Ottieni Visio Forma compreso il bambino
type: docs
weight: 110
url: /it/net/get-visio-shape-including-child/
description: Questa sezione spiega come ottenere la forma visio incluso il bambino con l'ID o il nome della forma con Aspose.Diagram.
---
### **Recupera una forma Visio che include un bambino**
Ogni forma in uno diagram ha un ID e un nome. L'ID è importante quando si programma con Visio: è il metodo principale per accedere ad una forma. Ogni forma conserva anche informazioni su quale master (stencil) è composta.

 UN[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) è un oggetto in un disegno Visio che potrebbe avere un padre o dei figli. La proprietà Shapes, esposta dalla classe Page, supporta una raccolta di oggetti Aspose.Diagram.Shape. La proprietà Shapes può essere utilizzata per recuperare informazioni su una forma.
#### **Recuperare Visio Shape Programming Sample**
Il seguente frammento di codice recupera la forma incluso il figlio. Si prega di controllare questo codice di esempio:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

