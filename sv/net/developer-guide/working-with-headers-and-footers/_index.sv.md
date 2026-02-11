---
title: Arbeta med sidhuvuden och sidfötter
type: docs
weight: 140
url: /sv/net/working-with-headers-and-footers/
description: Det här avsnittet förklarar hur du ställer in sidhuvuden och sidfötter för Microsoft Office Visio med Aspose.Diagram.
---
## **Hantera sidhuvuden och sidfötter i Visio-diagrammen**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) tillhandahåller en mekanism för att ställa in sidhuvuden och sidfötter för Microsoft Office Visio diagrammen. Utvecklare kan hämta eller ställa in textsträngen som visas på vänster, mitten och höger sida av ett dokuments sidhuvud/sidfot. De kan också ställa in sidhuvud och sidfotsmarginal tillsammans med teckensnittsegenskaperna för texten.
### **Ställa in egenskaper för sidhuvuden och sidfötter**
 De[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class-objekt erbjuder HeaderFooter-egenskap som gör det möjligt att hämta och ställa in sidhuvud och sidfotstext, teckensnitt och marginalvärden. Under förhandsgranskningen av Visio-ritningen kan användare klicka på länkknappen "Redigera sidhuvud och sidfot" i Microsoft Visio 2013 (i Microsoft Visio 2010 >> "Sidhuvud & fotfot"-knapp). Det finns några alternativ för att lägga till text som visas på skärmdumpen nedan. Användare kan hantera dessa egenskaper programmatiskt med Aspose.Diagram API enligt följande:
#### **Programmeringsexempel**
Följande kodbit hjälper till att hantera egenskaper för sidhuvuden och sidfötter.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
