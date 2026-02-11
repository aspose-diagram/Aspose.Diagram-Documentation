---
title: Arbeta med sidhuvuden och sidfötter
type: docs
weight: 150
url: /sv/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java tillhandahåller en mekanism för att ställa in sidhuvuden och sidfötter i diagrammen Microsoft Office Visio. Utvecklare kan hämta eller ställa in textsträngen som visas på vänster, mitten och höger sida av ett dokuments sidhuvud/sidfot. De kan också ställa in sidhuvud och sidfotsmarginal tillsammans med teckensnittsegenskaperna för texten.

{{% /alert %}} 
### **Ställa in egenskaper för sidhuvuden och sidfötter**
 De[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class-objekt erbjuder HeaderFooter-egenskap som gör det möjligt att hämta och ställa in sidhuvud och sidfotstext, teckensnitt och marginalvärden. Under förhandsgranskningen av Visio-ritningen kan användare klicka på länkknappen "Redigera sidhuvud och sidfot" i Microsoft Visio 2013 (i Microsoft Visio 2010 >> "Sidhuvud & fotfot"-knapp). Det finns några alternativ för att lägga till text som visas på skärmdumpen nedan. Användare kan hantera dessa egenskaper programmatiskt med Aspose.Diagram API enligt följande:

**Hantera sidhuvuden och sidfötter text, marginaler och teckensnittsegenskaper.** 

![todo:image_alt_text](working-with-headers-and-footers_1.png)

Följande kodbit hjälper till att hantera egenskaper för sidhuvuden och sidfötter.
#### **Programmeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
