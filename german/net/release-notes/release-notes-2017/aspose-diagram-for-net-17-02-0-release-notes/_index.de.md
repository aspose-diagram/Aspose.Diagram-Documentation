---
title: Aspose.Diagram for .NET 17.02.0 Versionshinweise
type: docs
weight: 110
url: /de/net/aspose-diagram-for-net-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für[Aspose.Diagram for .NET 17.02.0](https://www.nuget.org/packages/Aspose.Diagram/17.2.0).

{{% /alert %}} 
## **Verbesserungen und Änderungen**

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|DIAGRAMNET-50018|Unterstützung für CLS-konform hinzugefügt.|Neue Funktion|
|DIAGRAMNET-51110|Integriert mit Messgerät.|Neue Funktion|
|DIAGRAMNET-51143|Fähigkeit, die Gruppe einer bestimmten Form zu erhalten.|Neue Funktion|
|DIAGRAMNET-51144|Fähigkeit, das übergeordnete Element einer bestimmten Form zu erhalten.|Neue Funktion|
|DIAGRAMNET-50149|VSD zur PDF-Konvertierung wird der Hintergrundfarbton einer Gruppenform geändert.|Insekt|
|DIAGRAMNET-50579|VSDX in PDF-Konvertierung, falsche Hintergrundfarbe der Form.|Insekt|
|DIAGRAMNET-50984|Beim Umwandeln einer VSDX in PNG fehlen die Umrandungslinien der Tabelle.|Insekt|
|DIAGRAMNET-50985|Die Textelemente werden beim Konvertieren von VSDX in PNG nicht richtig ausgerichtet.|Insekt|
|DIAGRAMNET-50999|Rendern einer falschen Farbe von Formen beim Konvertieren von VSD in PNG.|Insekt|
|DIAGRAMNET-51002|Die HTMLSaveOptions.DefaultFont-Eigenschaft funktioniert nicht wie erwartet.|Insekt|
|DIAGRAMNET-51049|Die Farbe von Formen wird beim Konvertieren von VSD in HTML nicht korrekt wiedergegeben.|Insekt|
|DIAGRAMNET-51080|Die falsche Textausrichtung von Formen beim Speichern in EMF.|Insekt|
|DIAGRAMNET-51132|Die abgerundeten Ecken werden beim Konvertieren einer VSD in PDF geändert.|Insekt|
|DIAGRAMNET-51133|Das Layout des dynamischen Pfeilverbinders wird beim Konvertieren von VSD in PDF geändert.|Insekt|
|DIAGRAMNET-51135|Die Visio-Formen werden beim Konvertieren einer VSDX in PDF verschoben.|Insekt|
|DIAGRAMNET-51136|Der vertikale Text erscheint als horizontaler Text beim Konvertieren einer VSDX in PDF.|Insekt|
|DIAGRAMNET-51140|Das vertikale Textfeld überragt die Kante des Knotens, während VSDX in PDF konvertiert wird.|Insekt|
|DIAGRAMNET-51138|Beim Laden einer VSDX diagram ist ein Fehler aufgetreten.|Ausnahme|
|DIAGRAMNET-51139|Beim Konvertieren von VSDX in HTML ist der Fehler „Kann nicht auf Datei zugreifen“ aufgetreten.|Ausnahme|
|DIAGRAMNET-51148|NullReferenceException bei Diagram.Speichern, während VSD in HTML konvertiert wird.|Ausnahme|
|DIAGRAMNET-51149|NullReferenceException bei Diagram.Speichern, wenn die CustomProp.Name-Eigenschaft nicht festgelegt ist|Ausnahme|
## **Öffentliche API und rückwärts inkompatible Änderungen**
 Im Folgenden finden Sie eine Liste aller Änderungen, die an der öffentlichen API vorgenommen wurden, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder, sowie alle nicht abwärtskompatiblen Änderungen, die an Aspose.Diagram for .NET vorgenommen wurden. Wenn Sie Bedenken zu einer der aufgeführten Änderungen haben, äußern Sie diese bitte das[Aspose.Diagram Support-Forum](https://forum.aspose.com/c/diagram/17).
### **Fügt die Shape.ParentShape-Eigenschaft hinzu**
Die Shape.ParentShape-Eigenschaft ermöglicht es, die übergeordnete Form einer kürzlich verwendeten Form zu erhalten.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Shape parentShape = shape.ParentShape;

Console.WriteLine("Parent Shape's Properties:");

Console.WriteLine("Shape ID: " + parentShape.ID);

Console.WriteLine("Shape Name: " + parentShape.Name);

Console.WriteLine("Shape Type: " + parentShape.Type);

{{< /highlight >}}
### **Fügt die Shape.IsInGroup-Methode hinzu**
Die Shape.IsInGroup-Methode ermöglicht es zu erkennen, ob die aktuelle Form Teil einer Gruppenform ist.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Console.WriteLine("Is it in a Group: " + shape.IsInGroup());

{{< /highlight >}}
### **Fügt gemessene Klasse hinzu**
Die Metered-Klasse wird hinzugefügt. Es ermöglicht Entwicklern, die Evaluierungseinschränkungen von Aspose.Diagram API aufzuheben sowie API-Lizenzen zu verfolgen und zu warten. Es überwacht auch die regelmäßige Nutzung von Aspose.Diagram API.

{{< highlight "java" >}}

 // Initialize a Metered license class object

Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();

// apply public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **Anwendungsbeispiele**
Bitte überprüfen Sie die Liste der Hilfethemen, die in den Aspose.Diagram-Wiki-Dokumenten hinzugefügt wurden:

1. [Legen Sie öffentliche und private Schlüssel fest, um die gemessene Lizenz anzuwenden](/diagram/de/net/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [Rufen Sie die übergeordnete Form einer untergeordneten Form ab](/diagram/de/net/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [Überprüfen Sie, ob sich die Form Visio in einer Gruppe von Formen befindet](https://docs.aspose.com/diagram/net/group-convert-and-verify-shapes/)
