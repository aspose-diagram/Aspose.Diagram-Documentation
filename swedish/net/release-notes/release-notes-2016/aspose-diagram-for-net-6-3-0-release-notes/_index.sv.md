---
title: Aspose.Diagram for .NET 6.3.0 Release Notes
type: docs
weight: 90
url: /sv/net/aspose-diagram-for-net-6-3-0-release-notes/
---
## **Andra förbättringar och förändringar**

|**Nyckel** |**Sammanfattning** |**Kategori** |
|:- |:- |:- |
|DIAGRAMNET-50739 | Lägg till stöd för att detektera typen Visio diagram.| Ny funktion|
|DIAGRAMNET-50746 | Förhindra export av de dolda Visio-sidorna i PDF.| Ny funktion|
|DIAGRAMNET-50747 | Förhindra export av de dolda Visio-sidorna i HTML.| Ny funktion|
|DIAGRAMNET-50750 | Förhindra export av de dolda Visio-sidorna i PNG.| Ny funktion|
|DIAGRAMNET-50751 | Förhindra export av de dolda Visio-sidorna i JPEG.| Ny funktion|
|DIAGRAMNET-50752 | Förhindra export av de dolda Visio-sidorna i SVG.| Ny funktion|
|DIAGRAMNET-50753 | Förhindra export av de dolda Visio-sidorna i GIF.| Ny funktion|
|DIAGRAMNET-50754 | Förhindra export av de dolda Visio-sidorna i XPS.| Ny funktion|
|DIAGRAMNET-50541 |VSDX till PDF konvertering, hebreiska textobjekt återges i omvänd ordning.| Förbättring|
|DIAGRAMNET-50542 | VSD till PDF konvertering, arabiska ord förvandlas till bokstäver.| Förbättring|
|DIAGRAMNET-50682 | VSD till PDF export, tabellcellens text är delvis osynlig.| Insekt|
|DIAGRAMNET-50712 | VDX till PDF export - texten i olika former är felplacerad.| Insekt|
|DIAGRAMNET-50741 | VSD till SVG export saknar några Visio former.| Insekt|
|DIAGRAMNET-50742 | VSD till SVG export tillämpar inte den inre vita färgen på former.| Insekt|
|DIAGRAMNET-50744 |Öppna och spara rutin för VSDX har ändrat text till dummy-tecken.| Insekt|
|DIAGRAMNET-50745 | Öppna och spara rutin för VSDX har ändrat den prickade linjeformaren.| Insekt|
|DIAGRAMNET-50748 | VSD till PDF export - textobjekten är felplacerade.| Insekt|
|DIAGRAMNET-50763 | VSD till VDX exporten ger huvudelementfelet.| Insekt|
### **Offentlig API och bakåtinkompatibla ändringar**
Se listan för eventuella ändringar som gjorts för allmänheten API såsom tillagda, omdöpta, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp det på[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
#### **Lägg till klasserna FileFormatUtil och FileFormatInfo**
Dessa klasser ger programmatisk åtkomst för att upptäcka filtypen Visio.
#### **Lägger till DetectFileFormat-metoden i FileFormatUtil Class**
Den upptäcker och returnerar information om formatet för en lagrad Visio diagram i en fil.
#### **Lägger till FileFormatType Property i FileFormatInfo Class**
Den får det upptäckta filformatet.
#### **Lägger till LoadFormat-egenskap i FileFormatInfo**
Den får det upptäckta laddningsformatet.
#### **Lägger till ExportHiddenPage Property i klasserna SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions och PdfSaveOptions**
Den definierar om du behöver exportera de dolda Visio-sidorna eller inte.
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

- [Kontrollera exporten av dolda Visio-sidor när du sparar](/diagram/sv/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
- [Upptäck filformatet Visio](/diagram/sv/net/introduction/#detect-the-format-of-visio-file)
