---
title: Ställ in orientering och kontrollera exporten av dolda Visio sidor vid sparande
type: docs
weight: 20
url: /sv/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: Det här avsnittet förklarar hur du ställer in sidans layout med Aspose.Diagram.
---
## **Ändra en Visio sidlayout till stående eller liggande**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API tillåter utvecklare att ställa in orienteringen för Visio ritsidan programmatiskt. Det här hjälpämnet förklarar hur du utför denna uppgift.

 Aspose.Diagram for .NET API har[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också utskriftsegenskaperna. Fältet PrintPageOrientation i utskriftsegenskaperna gör det möjligt att rotera sidan. Den erbjuder tre alternativ som stående, liggande och samma som på skrivaren. Fältet PrintPageOrientation kan ställas in programmatiskt med Aspose.Diagram API.

Detta exempel fungerar enligt följande:

1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Extrahera en Visio sida
1. Ställ in orienteringen som Stående, Liggande eller samma som på skrivaren.
1. Spara Visio diagram.
### **Ställ in orienteringsprogrammeringsexempel**
Kodexemplet nedan visar hur du ställer in orienteringen för sidan Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Kontrollera exporten av dolda Visio-sidor när du sparar**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API tillåter utvecklare att inkludera eller utesluta dolda Visio sidor när de sparar diagram till PDF, HTML, bild (PNG, JPEG, GIF), 3416, 34716 och 34716 och 34716 Även de kan dölja Visio sidor med Aspose.Diagram API eftersom dess alternativ redan är tillgängligt via cellen UIVisibility på sidan ShapeSheet.
### **Göm en sida i Visio Diagram och ange exportalternativ**
 Aspose.Diagram for .NET API har[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också sidegenskaperna. UIVisibility-fältet i sidegenskaperna gör det möjligt att dölja sidan. Utvecklare kan sedan använda egenskapen ExportHiddenPage som läggs till i klasserna SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions och PdfSaveOptions.
#### **Ställ in exportalternativet för PDF**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **Ställ in exportalternativet för HTML**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Ställ in exportalternativet för bild**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till bildformat.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **Ställ in exportalternativet för SVG**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **Ställ in exportalternativet för XPS**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
