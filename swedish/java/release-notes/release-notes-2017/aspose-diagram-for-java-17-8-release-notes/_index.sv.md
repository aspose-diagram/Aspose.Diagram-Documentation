---
title: Aspose.Diagram for Java 17.8 Release Notes
type: docs
weight: 50
url: /sv/java/aspose-diagram-for-java-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for Java 17.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-8-release-notes/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMJAVA-50412|Saknade former vid konvertering av en VST till PNG.|Insekt|
|DIAGRAMJAVA-50497|Utgång VSDX - felaktig layout av alla anslutningsledningar.|Insekt|
|DIAGRAMJAVA-50500|Utdata VSDX - den manuellt tillagda formstorleken ändras inte.|Insekt|
|DIAGRAMJAVA-50511|Utgång VSDX - felplacerad text för den dynamiska kontakten.|Insekt|
|DIAGRAMJAVA-50516|Utgång VSDX - förbindelselinjen som går genom en annan form.|Insekt|
|DIAGRAMJAVA-50517|Utgång VSDX - beslutsformen blir allt större.|Insekt|
|DIAGRAMJAVA-50520|Det går inte att ställa in överlappningsbeteendet för anslutande linjer i en VSDX-ritning.|Insekt|
|DIAGRAMJAVA-50521|Utgång VSDX - felaktig layout av anslutningsledningen.|Insekt|
|DIAGRAMJAVA-50522|Utdata PNG - formtexten går utanför gränsen.|Insekt|
|DIAGRAMJAVA-50523|Utgång VSDX - felaktig layout av anslutningsledningen.|Insekt|
|DIAGRAMJAVA-50525|Utdata VSDX - breddformeln för någon form bevaras inte.|Insekt|
|DIAGRAMJAVA-50528|Utgång VSDX - felaktig storlek på formen.|Insekt|
|DIAGRAMJAVA-50529|Utdata VSDX - bevara formlerna för textomvandlingsavsnittet.|Insekt|
|DIAGRAMJAVA-50531|Utdata VSDX - formernas layout är inte enligt bredden och höjden i formbladet.|Insekt|
|DIAGRAMJAVA-50533|Utgång VSDX - felaktig layout av anslutningsledningen.|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Se listan för eventuella ändringar som gjorts för allmänheten API såsom tillagda, omdöpta, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for Java. Om du har frågor om någon ändring i listan, vänligen ta upp det på[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till Quality-medlem i SVGSaveOptions-klassen**
Den får eller ställer in ett värde som bestämmer kvaliteten på de genererade bilderna.

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.setQuality(100);

// save drawing in the SVG format

diagram.save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Lägger till connectShapesViaConnectorIndex-metoden i klassen Page**
Det gör det möjligt att ansluta former med hjälp av anslutningsindex.

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Shape shape1 = diagram.getPages().get(0).getShapes().getShape(1);

Shape shape2 = diagram.getPages().get(0).getShapes().getShape(2);

// add connector shapes

Shape connector1 = new Shape();

long connecter1Id = diagram.addShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.getPages().get(0).connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

// save drawing

diagram.save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Använd anslutningsindex för att koppla samman former](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Användning av SVG Spara alternativ](https://docs.aspose.com/diagram/java/save-visio-document/#use-of-the-svg-save-options)
