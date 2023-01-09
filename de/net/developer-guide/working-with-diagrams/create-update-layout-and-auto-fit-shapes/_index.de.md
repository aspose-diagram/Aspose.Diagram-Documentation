---
title: Formen erstellen, aktualisieren, anordnen und automatisch anpassen
type: docs
weight: 10
url: /de/net/create-update-layout-and-auto-fit-shapes/
description: Verwenden Sie C# Diagram API zum Erstellen, Aktualisieren und automatischen Layout von Formen in Visio-Dateien mit C# in Ihren Anwendungen. Vollständige Anleitung mit C# Codebeispielen.
---
## **Erstellen einer Diagram**
 Mit Aspose.Diagram for .NET können Sie Microsoft Visio Diagramme aus Ihren eigenen Anwendungen lesen und erstellen, ohne Microsoft Office Automatisierung. Der erste Schritt beim Erstellen neuer Dokumente ist das Erstellen einer diagram. Dann[Fügen Sie Formen und Verbinder hinzu](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)um die diagram aufzubauen. Verwenden Sie den Standardkonstruktor von[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, um eine neue diagram zu erstellen.
### **Programmierbeispiel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}
## **Layoutformen im Flussdiagrammstil**
 Bei bestimmten Arten von verbundenen Zeichnungen, wie z. B. Flussdiagrammen und Netzwerkdiagrammen, können Sie die verwenden**Layoutformen** Funktion zum automatischen Positionieren von Formen. Die automatische Positionierung ist schneller als das manuelle Ziehen jeder Form an eine neue Position.

Wenn Sie beispielsweise ein großes Flussdiagramm aktualisieren, um einen neuen Prozess einzuschließen, können Sie die Shapes, aus denen der Prozess besteht, hinzufügen und verbinden und dann die Layoutfunktion verwenden, um die aktualisierte Zeichnung automatisch zu gestalten.

 Die Layout-Methode, verfügbar gemacht durch die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Die Klasse legt die Formen an und/oder leitet die Anschlüsse auf allen Seiten von diagram um. Diese Methode akzeptiert eine[LayoutOptionen](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)Objekt als Argument. Verwenden Sie die verschiedenen Eigenschaften, die von der LayoutOptions-Klasse verfügbar gemacht werden, um Formen automatisch anzuordnen.

Das Bild unten zeigt den diagram, der von den Codeausschnitten in diesem Artikel geladen wird, bevor das automatische Layout angewendet wird. Die Codeschnipsel zeigen, wie man sich bewirbt[Flussdiagramm-Layouts](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) und[kompakte Baumlayouts](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**Die Quelle diagram.**

![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_1.png)

Die Code-Snippets in diesem Artikel verwenden die Quelle diagram und wenden mehrere Arten von automatischem Layout darauf an, wobei sie jeweils in einer separaten Datei gespeichert werden.

|<p>**Layoutformen von unten nach oben** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layoutformen von oben nach unten** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Layoutformen von links nach rechts** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layoutformen von rechts nach links** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_5.png)</p>|
So gestalten Sie Formen im Flussdiagrammstil:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse und legen Sie die Eigenschaften für den Flussdiagrammstil fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnung Visio zu schreiben.
### **Programmierbeispiel im Flussdiagrammstil**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.cs" >}}
### **Anordnen von Formen im kompakten Baumstil**
 Der kompakte Baumlayoutstil versucht, eine Baumstruktur aufzubauen. Es verwendet die gleiche Eingabedatei wie die[Beispiel oben](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)und speichert in mehreren verschiedenen kompakten Baumstilen.

|<p>**Kompaktes Baumlayout - unten und rechts** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompaktes Baumlayout - unten und links** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompaktes Baumlayout - rechts und unten** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompaktes Baumlayout - links und unten** </p><p>![todo: Bild_alt_Text](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Formen im kompakten Baumstil anordnen:

1.  Erstellen Sie eine Instanz der[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse, und legen Sie kompakte Baumstileigenschaften fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Datei Visio zu schreiben.
#### **Kompaktes Programmierbeispiel im Baumstil**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.cs" >}}
## **Passen Sie die Visio Diagram automatisch an**
 Aspose.Diagram API unterstützt die automatische Anpassung der Zeichnung Visio. Diese Feature-Operation hilft, äußere Formen innerhalb der Visio-Seitenbegrenzung zu bringen. Aspose.Diagram for .NET API hat die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Das[DiagrammSaveOptions](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) -Klasse macht die AutoFitPageToDrawingContent-Eigenschaft verfügbar, um die Visio-Zeichnung automatisch anzupassen.

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Erstellen Sie ein Objekt der Klasse DiagramSaveOptions und übergeben Sie das resultierende Dateiformat.
1. Legen Sie die AutoFitPageToDrawingContent-Eigenschaft des DiagramSaveOptions-Objekts fest.
1. Rufen Sie die Save-Methode des Klassenobjekts Diagram auf und übergeben Sie auch den vollständigen Dateipfad und das DiagramSaveOptions-Objekt.
### **Programmierbeispiel für automatische Anpassung**
Der folgende Beispielcode zeigt, wie Formen in Visio diagram automatisch angepasst werden.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.cs" >}}
## **Arbeiten mit VBA-Projekt**
### **Ändern Sie den VBA-Modulcode in Visio Diagram**
 Dieser Artikel zeigt, wie Sie einen VBA-Modulcode automatisch mit Aspose.Diagram for .NET ändern. Wir haben hinzugefügt[VbaModul](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProjekt](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) und[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) Klassen. Diese Klassen helfen dabei, die Kontrolle über das VBA-Projekt zu erlangen. Entwickler können VBA-Modulcode extrahieren und ändern.
### **Programmierbeispiel für VBA-Modulcode ändern**
Bitte überprüfen Sie dieses Codebeispiel:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-ModifyVBAModule-ModifyVBAModule.cs" >}}
### **Entfernen Sie alle Makros aus Visio Diagram**
 Aspose.Diagram for .NET ermöglicht Entwicklern das Entfernen aller Makros aus Visio diagram. Die VbProjectData-Eigenschaft, die von der[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse können Sie alle Makros aus der Zeichnung Visio entfernen.
### **Programmierbeispiel für alle Makros entfernen**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.cs" >}}
## **Erstellen eines neuen Diagram mit VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)ermöglicht Entwicklern das Erstellen und Arbeiten mit Microsoft Office Visio Diagrammen und die Integration von Funktionen in ihre Softwareanwendungen. Es gibt andere Möglichkeiten, mit Visio-Dateien zu arbeiten, am häufigsten Microsoft-Automatisierung. Leider hat das einige Einschränkungen. Aspose.Diagram ist leistungsstark und schnell und arbeitet selbstständig ohne Microsoft Office Installation.

 Dieser Migrationsartikel zeigt die Verwendung von first[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) und dann[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) um eine neue diagram zu erstellen und ihr einige Formen hinzuzufügen. Sie werden feststellen, dass der Code Aspose.Diagram kürzer als der VSTO-Code ist. Sie können den Code gerne als Grundlage für Ihre eigene Entwicklung verwenden und ihn Ihren Anforderungen entsprechend erweitern. Mit VSTO können Sie mit Microsoft-Visio-Dateien programmieren. So erstellen Sie eine neue diagram:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Erstellen Sie eine leere diagram.
1. Fügen Sie Formen aus Visio-Mastern (Schablonen) hinzu.
1. Speichern Sie die Datei als VDX.
### **Neues Diagram mit VSTO-Programmierbeispiel erstellen**
{{% alert color="primary" %}}

mit Visio = Microsoft.Office.Interop.Visio;
Importe Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Beispiel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithVSTO-CreatingDiagramWithVSTO.cs" >}}
## **Erstellen einer neuen Diagram mit Aspose.Diagram for .NET**
Mit Aspose.Diagram API benötigen Entwickler keine Microsoft Office Visio Installation auf der Maschine und können unabhängig von Microsoft Office Automation arbeiten.

So erstellen Sie eine neue diagram:

1. Erstellen Sie eine leere diagram.
1. Fügen Sie Formen aus Visio-Mastern (Schablonen) hinzu.
1. Speichern Sie die Datei als VDX.
### **Neu Diagram mit Aspose.Diagram for .NET Programmierbeispiel**
{{% alert color="primary" %}}

mit Aspose.Diagram;
Importiert Aspose.Diagram

{{% /alert %}}

Beispiel:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithAspose-CreatingDiagramWithAspose.cs" >}}
## **Shape-Eigenschaften aktualisieren**
 Bei der Arbeit mit Microsoft Visio Diagrammen können Benutzer Formattribute aktualisieren, einschließlich Text, Stil, Position, Höhe und Breite. Als Softwareentwickler, der mit Visio-Dateien arbeitet, werden Sie aufgefordert, dies programmgesteuert zu tun. Die gute Nachricht ist, dass es möglich ist, entweder die Mechanismen zum Programmieren mit Visio-Dateien zu verwenden, die Microsoft bereitstellt, VSTO, oder zu verwenden[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Das folgende Thema zeigt die Verwendung[VSTO](https://products.aspose.com/diagram/net/) und[Aspose.Diagram](https://products.aspose.com/diagram/net/) Formeigenschaften zu aktualisieren. Die folgenden Codeausschnitte zeigen, wie Formeigenschaften für VSTO und Aspose.Diagram for .NET aktualisiert werden. Sie können den Code gerne verwenden und auf Ihre spezielle Situation anwenden.
### **Aktualisieren von Shape-Eigenschaften mit VSTO**
Mit VSTO können Sie mit Microsoft Visio-Dateien programmieren. So aktualisieren Sie Formeigenschaften:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Öffnen Sie eine vorhandene Visio VSD-Datei.
1. Finden Sie die gewünschte Form.
1. Aktualisieren Sie die Formeigenschaften (Text, Textstil, Position und Größe).
1. Speichern Sie die Datei als VDX.
#### **Aktualisieren von Shape-Eigenschaften mit VSTO-Programmierbeispiel**
{{% alert color="primary" %}}

mit Visio = Microsoft.Office.Interop.Visio;
Importe Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Beispiel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithVSTO-UpdateShapePropsWithVSTO.cs" >}}
### **Aktualisieren der Shape-Eigenschaften mit Aspose.Diagram for .NET**
Mit Aspose.Diagram API benötigen Entwickler keine Microsoft Office Visio auf der Maschine und können unabhängig von Microsoft Office Automation arbeiten.

So aktualisieren Sie Formeigenschaften mit Aspose.Diagram for .NET:

1. Öffnen Sie eine vorhandene Visio VSD-Datei.
1. Finden Sie die gewünschte Form.
1. Aktualisieren Sie die Formeigenschaften (Text, Textstil, Position und Größe).
1. Speichern Sie die Datei als VDX.
#### **Aktualisieren von Shape-Eigenschaften mit Aspose.Diagram for .NET Programmierbeispiel**
{{% alert color="primary" %}}

mit Aspose.Diagram;
Importiert Aspose.Diagram

{{% /alert %}}

**Beispiel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithAspose-UpdateShapePropsWithAspose.cs" >}}
