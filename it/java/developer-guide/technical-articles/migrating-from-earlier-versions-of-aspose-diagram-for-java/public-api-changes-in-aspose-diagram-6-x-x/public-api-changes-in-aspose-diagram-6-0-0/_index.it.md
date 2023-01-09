---
title: Pubblico API Modifiche in Aspose.Diagram 6.0.0
type: docs
weight: 50
url: /it/java/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche al Aspose.Diagram API dalla versione 5.9.0 alla 6.0.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **Il metodo isGlued viene aggiunto nella classe Shape**
Il metodo isGlued accetta un oggetto forma come parametro per determinare se le due forme sono incollate o meno.
Codice di esempio:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are glued

boolean glued = ShapedOne.isGlued(ShapedTwo);

{{< /highlight >}}
### **Il metodo isConnected viene aggiunto nella classe Shape**
Il metodo isConnected accetta un oggetto forma come parametro per determinare se le due forme sono connesse o meno.
Codice di esempio:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are connected

boolean connected = ShapedOne.isConnected(ShapedTwo);

{{< /highlight >}}
