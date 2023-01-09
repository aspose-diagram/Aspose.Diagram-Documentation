---
title: Pubblico API Modifiche Aspose.Diagram 16.12.0
type: docs
weight: 10
url: /it/java/public-api-changes-in-aspose-diagram-16-12-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 16.11.0 alla 16.12.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **Modifica le proprietà di un gradiente**
Gli sviluppatori possono recuperare un'interruzione del gradiente e quindi modificarne le proprietà. Abbiamo aggiunto[GradientFill](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)e[GradientStop](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientstop)classi per questo scopo. Si prega di controllare l'esempio di codice:

**Java**

{{< highlight "csharp" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("C:\\temp\\MyVisio.vsdx");

// get page by name

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the gradient fill properties

GradientFill gradientfill = shape.getFill().getGradientFill();

// get the gradient stops

GradientStopCollection stops = gradientfill.getGradientStops();

// get the gradient stop by index

GradientStop stop = stops.get(0);

// set gradient stop properties

stop.getColor().getUfe().setF("");

stop.getPosition().setValue(0.5);

gradientfill.getGradientDir().setValue(GradientFillDir.RECTANGLE_FROM_BOTTOM_RIGHT);

gradientfill.getGradientAngle().setValue(0.7853981633974501);

// save the Visio drawing

diagram.save("C:\\temp\\Output.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
