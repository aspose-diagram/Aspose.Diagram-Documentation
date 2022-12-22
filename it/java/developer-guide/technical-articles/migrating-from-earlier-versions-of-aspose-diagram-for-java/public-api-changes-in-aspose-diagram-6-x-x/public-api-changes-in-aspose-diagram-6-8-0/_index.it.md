---
title: Pubblico API Modifiche Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /it/java/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 6.7.0 alla 6.8.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **Inserisci un controllo ActiveX**
 Gli sviluppatori possono inserire un controllo ActiveX nel Visio diagram. Abbiamo aggiunto il metodo addActiveXControl nel[Pagina](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) classe. Si prega di controllare questo esempio di codice:

**Java**

{{< highlight "java" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);

// save diagram

diagram.save("C:\\temp\\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Imposta la casella di controllo del colore del livello**
Gli sviluppatori possono impostare o ottenere il Color CheckBox di Layer utilizzando Aspose.Diagram API. Controlla questo esempio di codice:

**Java**

{{< highlight "java" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// Get Visio page

Page page = diagram.getPages().getPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// set Layer name

layer.getName().setValue("Layer1");

// Set Layer Visibility

layer.getVisible().setValue(BOOL.TRUE);

// set the color checkbox of Layer

layer.setColorChecked(BOOL.TRUE);

// Add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer);

// get shape by ID

Shape shape = page.getShapes().getShape(3);

// assign shape to this new Layer

shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));

// save diagram

diagram.save("c:\\temp\\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Aggiunge la proprietà InheritFill nella classe Shape**
Gli sviluppatori possono ottenere o impostare la proprietà inherit fill. Abbiamo aggiunto la proprietà InheritFill nella classe Shape. Si prega di controllare questo esempio di codice:

**Java**

{{< highlight "java" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page by ID

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the fill formatting values

System.out.println(shape.getInheritFill().getFillBkgnd().getValue());

System.out.println(shape.getInheritFill().getFillForegnd().getValue());

System.out.println(shape.getInheritFill().getFillPattern().getValue());

{{< /highlight >}}
