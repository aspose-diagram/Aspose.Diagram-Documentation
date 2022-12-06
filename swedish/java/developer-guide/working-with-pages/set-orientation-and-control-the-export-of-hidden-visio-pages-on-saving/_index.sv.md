---
title: Ställ in orientering och kontrollera exporten av dolda Visio sidor vid sparande
type: docs
weight: 20
url: /sv/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Ändra en Visio sidlayout till stående eller liggande**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API tillåter utvecklare att ställa in orienteringen för Visio ritsidan programmatiskt. Det här hjälpämnet förklarar hur du utför denna uppgift.

 Aspose.Diagram for Java API har[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också utskriftsegenskaperna. Fältet PrintPageOrientation i utskriftsegenskaperna gör det möjligt att rotera sidan. Den erbjuder tre alternativ som stående, liggande och samma som på skrivaren. Fältet PrintPageOrientation kan ställas in programmatiskt med Aspose.Diagram API.

Detta exempel fungerar enligt följande:

1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Extrahera en Visio sida
1. Ställ in orienteringen som Stående, Liggande eller samma som på skrivaren.
1. Spara Visio diagram.
### **Ställ in orienteringsprogrammeringsexempel**
Kodexemplet nedan visar hur du ställer in orienteringen för sidan Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-SetVisioPageOrientation-SetVisioPageOrientation.java" >}}
## **Kontrollera exporten av dolda Visio-sidor när du sparar**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API tillåter utvecklare att inkludera eller utesluta dolda Visio-sidor när de sparar diagram till PDF-, HTML-, bild- (PNG, JPEG, GIF), SVG- och XPS-filer. Även de kan dölja Visio sidor med Aspose.Diagram API eftersom dess alternativ redan är tillgängligt via cellen UIVisibility på sidan ShapeSheet.
### **Göm en sida i Visio Diagram och ange exportalternativ**
 Aspose.Diagram for Java API har[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också sidegenskaperna. UIVisibility-fältet i sidegenskaperna gör det möjligt att dölja sidan. Utvecklare kan sedan använda egenskapen ExportHiddenPage som läggs till i klasserna SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions och PdfSaveOptions.
#### **Ställ in exportalternativet för PDF**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till PDF-format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExporToHiddenVisioPagesToPdf-ExporToHiddenVisioPagesToPdf.java" >}}
#### **Ställ in exportalternativet för HTML**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till HTML-format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToHtml-ExportOfHiddenVisioPagesToHtml.java" >}}
#### **Ställ in exportalternativet för bild**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till bildformat.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.java" >}}
#### **Ställ in exportalternativet för SVG**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till SVG-format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.java" >}}
