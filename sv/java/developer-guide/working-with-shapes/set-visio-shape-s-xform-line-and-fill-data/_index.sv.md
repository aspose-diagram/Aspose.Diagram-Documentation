---
title: Ställ in Visio Shapes XForm, Line och Fill Data
type: docs
weight: 70
url: /sv/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Ställa in XForm-data**
 XForm-elementet är en del av XML-schemat Microsoft Visio. XForm anger en forms position, till exempel bredd, höjd, rotation och om formen har vänts. De[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) egendom, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass, stöder objektet Aspose.Diagram.XForm. XForm-egenskapen kan användas för att hämta eller uppdatera en forms XForm-data. Kodexemplen i den här artikeln ändrar PinX (X-koordinat) och PinY (Y-koordinat) XForm-värden för att flytta formerna på sidan.

**Ingång diagram** 

![todo:image_alt_text](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram efter den** **PinX** **och** **PinY** **värden har ändrats** 

![todo:image_alt_text](set-visio-shape-s-xform-line-and-fill-data_2.png)

Processen för att uppdatera XForm-data är:

1. Ladda en diagram.# Hitta en viss form.# Uppdatera formens XForm-data.
1. Spara diagram.
### **Programmeringsexempel**
Kodavsnittet nedan visar hur du uppdaterar en forms XForm-data. Koden letar efter en process för formnamn, med form-ID 1, och ställer in dess X- och Y-koordinater till 5.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Ställ in Visio Shape's Line Data**
Former kan formateras på flera sätt. Den här artikeln visar hur du anger en linjes attribut.

Microsoft Visio låter användare formatera linjer på olika sätt. Aspose.Diagram for Java stöder:

- Vikt: en linjes tjocklek.
- Färg: ställ in formens linjefärg.
- Linjefärgstransparens: ställ in formens linjefärgtransparens i procent.
- Mönster: definierar om linjen är heldragen, streckad eller har ett annat mönster.
- Avrundning: radien på hörnen.
- Start- och slutpilar: ange om linjen har pilar.
- Början och slutet pilstorlekar: ställ in pilstorlekarna.
- Cap: avrundningen av linjen slutar.
### **Ändra linjefärg, vikt, strecktyp, transparens, avrundning, piltyp och pilstorlek för en forms kant**
 De[Linje](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) egendom, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)klass, stöder objektet Aspose.Diagram.Line. Den här egenskapen kan användas för att hämta eller uppdatera en forms linjedata.
#### **Linjedataprogrammeringsexempel**
Följande kodbit uppdaterar formens linjedata.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Ställ in Visio Shape's Fill Data**
Former kan formateras på flera sätt. Det här avsnittet beskriver hur du anger en forms fyllning.

 Microsoft Office Visio låter användare formatera fyllningar på olika sätt. De[Fylla](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) klass av Aspose.Diagram for Java API stöder inställning:

- Bakgrunds- och förgrundsfärger.
- Genomskinlighet.
- Fyllningsmönster.
- Skuggor.
### **Ställa in fyllningsvärden**
Fill-egenskapen, exponerad av Shape-klassen, stöder objektet Aspose.Diagram.Fill. Fill-egenskapen kan användas för att hämta eller uppdatera en forms fyllningsdata.

|<p>**Ingången diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/OrhEecb.png)</p>|<p>**diagram efter att ha ändrat fyllningsfärgen** </p><p>![todo:image_alt_text](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Fyll i dataprogrammeringsexempel**
Följande kodavsnitt uppdaterar en forms fyllningsdata. Koden letar efter en form som heter rektangel, med form-ID 1, och ställer in fyllningsbakgrunds- och förgrundsfärgerna.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Hämta ärvd fyllningsdata för en Visio-form**
Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvd fyllningsdata för en Visio-form. Egenskapen InheritFill, exponerad av Shape-klassen, innehåller fyllningsformateringsvärdena för formen som ärver av den överordnade stilen och masterformen.
#### **Hämta ärvt fyllningsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda fyllningsdata. Kontrollera denna exempelkod:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}

