---
title: Öffentlich API Änderungen in Aspose.Diagram 6.3.0
type: docs
weight: 30
url: /de/net/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.Diagram API von Version 6.0.0 zu 6.3.0, die für Modul-/Anwendungsentwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.Diagram.

{{% /alert %}} 
## **Erkennen Sie das Format einer Visio-Datei**
**Verschiedene Klassen, Methoden und Eigenschaften werden hinzugefügt, um das Format zu erkennen**
- **Fügen Sie die Klassen FileFormatUtil und FileFormatInfo hinzu** 
 - Diese Klassen gewähren programmgesteuerten Zugriff, um den Dateityp Visio zu erkennen.
- **Fügt die DetectFileFormat-Methode in der FileFormatUtil-Klasse hinzu** 
 - Es erkennt und gibt die Informationen über das Format einer gespeicherten Visio diagram in einer Datei zurück.
- **Fügt FileFormatType-Eigenschaft in FileFormatInfo-Klasse hinzu** 
 - Es erhält das erkannte Dateiformat.
- **Fügt LoadFormat-Eigenschaft in FileFormatInfo hinzu** 
 - Es erhält das erkannte Ladeformat.

 Entwickler können das Format jeder Visio-Datei leicht erkennen. Dieses Hilfethema veranschaulicht, wie Sie das Dateiformat Visio (mithilfe eines Dateipfads oder Streams) erkennen und seine Erweiterung überprüfen:[Erkennen Sie das Format der Datei Visio](/diagram/de/net/introduction/#detect-the-format-of-visio-file)
## **Steuern Sie den Export versteckter Visio-Seiten beim Speichern**
**Fügt die ExportHiddenPage-Eigenschaft in den Klassen SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions und PdfSaveOptions hinzu**
- Es definiert, ob die versteckten Visio-Seiten exportiert werden müssen oder nicht.

 Entwickler können versteckte Visio-Seiten beim Speichern von Visio diagram in PDF-, HTML-, Bild- (PNG, JPEG, GIF), SVG- und XPS-Dateien einschließen oder ausschließen. Dieses Hilfethema zeigt, wie das geht:[Steuern Sie den Export versteckter Visio-Seiten beim Speichern](/diagram/de/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
