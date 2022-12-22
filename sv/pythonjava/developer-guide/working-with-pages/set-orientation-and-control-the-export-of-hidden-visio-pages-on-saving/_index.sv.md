---
title: Ställ in orientering och kontrollera exporten av dolda Visio sidor vid sparande
type: docs
weight: 20
url: /sv/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Ändra en Visio sidlayout till stående eller liggande**
Aspose.Diagram för Python via Java API låter utvecklare ställa in orienteringen för Visio ritsidan programmatiskt. Det här hjälpämnet förklarar hur du utför denna uppgift.

Aspose.Diagram för Python via Java API har klassen `Page` som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också utskriftsegenskaperna. Fältet `PrintPageOrientation` för utskriftsegenskaper gör det möjligt att rotera sidan. Den erbjuder tre alternativ som stående, liggande och samma som på skrivaren. Fältet PrintPageOrientation kan ställas in programmatiskt med Aspose.Diagram för Python via Java API.

Detta exempel fungerar enligt följande:

1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Extrahera en Visio sida
1. Ställ in orienteringen som Stående, Liggande eller samma som på skrivaren.
1. Spara Visio diagram.

### **Ställ in orienteringsprogrammeringsexempel**
Kodexemplet nedan visar hur du ställer in orienteringen för sidan Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-SetVisioPageOrientation.py" >}}

## **Kontrollera exporten av dolda Visio-sidor när du sparar**
Aspose.Diagram for Python via Java API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Till och med de kan dölja Visio sidor med Aspose.Diagram för Python via Java API eftersom dess alternativ redan är tillgängligt via cellen UIVisibility i sidan ShapeSheet.

### **Göm en sida i Visio Diagram och ange exportalternativ**
Aspose.Diagram för Python via Java API har klassen `Page` som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också sidegenskaperna. Fältet `UIVisibility` i sidegenskaper gör det möjligt att dölja sidan. Utvecklare kan sedan använda egendomen `exportHiddenPage` som läggs till i klasserna `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` och `PdfSaveOptions`.

#### **Ställ in exportalternativet för PDF**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till PDF.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExporToHiddenVisioPagesToPdf.py" >}}

#### **Ställ in exportalternativet för HTML**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till HTML.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToHtml.py" >}}

#### **Ställ in exportalternativet för bild**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till bildformat.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToImage.py" >}}

#### **Ställ in exportalternativet för SVG**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till SVG.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToSVG.py" >}}
