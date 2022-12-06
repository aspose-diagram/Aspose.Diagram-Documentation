---
title: Aspose.Diagram for .NET 6.3.0 Versionshinweise
type: docs
weight: 90
url: /de/net/aspose-diagram-for-net-6-3-0-release-notes/
---
## **Andere Verbesserungen und Änderungen**

|**Taste** |**Zusammenfassung** |**Kategorie** |
|:- |:- |:- |
|DIAGRAMNET-50739 | Unterstützung für die Erkennung des Typs Visio diagram hinzugefügt.| Neue Funktion|
|DIAGRAMNET-50746 | Export der versteckten Visio-Seiten im PDF verhindern.| Neue Funktion|
|DIAGRAMNET-50747 | Verhindern Sie den Export der versteckten Visio-Seiten im HTML.| Neue Funktion|
|DIAGRAMNET-50750 | Verhindern Sie den Export der versteckten Visio-Seiten im PNG.| Neue Funktion|
|DIAGRAMNET-50751 | Verhindern Sie den Export der versteckten Visio-Seiten im JPEG.| Neue Funktion|
|DIAGRAMNET-50752 | Export der versteckten Visio-Seiten im SVG verhindern.| Neue Funktion|
|DIAGRAMNET-50753 | Export der versteckten Visio-Seiten im GIF verhindern.| Neue Funktion|
|DIAGRAMNET-50754 | Export der versteckten Visio-Seiten im XPS verhindern.| Neue Funktion|
|DIAGRAMNET-50541 | VSDX in PDF-Konvertierung werden hebräische Textelemente in umgekehrter Reihenfolge gerendert.| Erweiterung|
|DIAGRAMNET-50542 | VSD in PDF-Konvertierung, arabisches Wort wird zu Buchstaben.| Erweiterung|
|DIAGRAMNET-50682 | VSD zum PDF-Export, der Text der Tabellenzelle ist teilweise unsichtbar.| Insekt|
|DIAGRAMNET-50712 | VDX in PDF-Export - der Text verschiedener Formen ist falsch platziert.| Insekt|
|DIAGRAMNET-50741 | Beim VSD-zu-SVG-Export fehlen einige Visio-Formen.| Insekt|
|DIAGRAMNET-50742 | VSD zum SVG-Export wendet die innere weiße Farbe von Formen nicht an.| Insekt|
|DIAGRAMNET-50744 |Öffnen- und Speichern-Routine von VSDX hat Text in Dummy-Zeichen geändert.| Insekt|
|DIAGRAMNET-50745 | Die Open-and-Save-Routine von VSDX hat den gepunkteten Linienformer geändert.| Insekt|
|DIAGRAMNET-50748 | VSD zum PDF-Export - die Textelemente sind falsch platziert.| Insekt|
|DIAGRAMNET-50763 | VSD bis VDX Export löst den Master-Elementfehler aus.| Insekt|
### **Öffentliche API und rückwärts inkompatible Änderungen**
Sehen Sie sich die Liste für alle Änderungen an, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
#### **Fügen Sie die Klassen FileFormatUtil und FileFormatInfo hinzu**
Diese Klassen gewähren programmgesteuerten Zugriff, um den Dateityp Visio zu erkennen.
#### **Fügt die DetectFileFormat-Methode in der FileFormatUtil-Klasse hinzu**
Es erkennt und gibt die Informationen über das Format einer gespeicherten Visio diagram in einer Datei zurück.
#### **Fügt FileFormatType-Eigenschaft in FileFormatInfo-Klasse hinzu**
Es erhält das erkannte Dateiformat.
#### **Fügt LoadFormat-Eigenschaft in FileFormatInfo hinzu**
Es erhält das erkannte Ladeformat.
#### **Fügt die ExportHiddenPage-Eigenschaft in den Klassen SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions und PdfSaveOptions hinzu**
Es definiert, ob die versteckten Visio-Seiten exportiert werden müssen oder nicht.
### **Anwendungsbeispiele**
Bitte überprüfen Sie die Liste der Hilfethemen, die in den Aspose.Diagram-Wiki-Dokumenten hinzugefügt wurden:

- [Steuern Sie den Export versteckter Visio-Seiten beim Speichern](/diagram/de/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
- [Erkennen Sie das Format der Datei Visio](/diagram/de/net/introduction/#detect-the-format-of-visio-file)
