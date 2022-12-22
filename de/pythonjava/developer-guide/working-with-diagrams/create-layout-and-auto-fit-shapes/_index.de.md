﻿---
title: Formen erstellen, gestalten und automatisch anpassen
type: docs
weight: 10
url: /de/python-java/create-layout-and-auto-fit-shapes/
---
## **Erstellen einer Diagram**
Aspose.Diagram for Python via Java lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [Fügen Sie Formen und Verbinder hinzu](/diagram/de/python-java/add-and-connect-visio-shapes/) um die diagram aufzubauen. Verwenden Sie den Standardkonstruktor der Diagram-Klasse, um eine neue diagram zu erstellen.
### **Programmierbeispiel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-CreateDiagram.py" >}}
## **Layoutformen im Flussdiagrammstil**
 Bei bestimmten Arten von verbundenen Zeichnungen, wie z. B. Flussdiagrammen und Netzwerkdiagrammen, können Sie die verwenden**Layoutformen** Funktion zum automatischen Positionieren von Formen. Die automatische Positionierung ist schneller als das manuelle Ziehen jeder Form an eine neue Position.

Wenn Sie beispielsweise ein großes Flussdiagramm aktualisieren, um einen neuen Prozess einzuschließen, können Sie die Shapes, aus denen der Prozess besteht, hinzufügen und verbinden und dann die Layoutfunktion verwenden, um die aktualisierte Zeichnung automatisch zu gestalten.

Die Layout-Methode, die von der Diagram-Klasse verfügbar gemacht wird, legt die Formen an und/oder leitet die Konnektoren auf allen Seiten von diagram um. Diese Methode akzeptiert ein LayoutOptions-Objekt als Argument. Verwenden Sie die verschiedenen Eigenschaften, die von der LayoutOptions-Klasse verfügbar gemacht werden, um Formen automatisch anzuordnen.

Das Bild unten zeigt den diagram, der von den Codeausschnitten in diesem Artikel geladen wird, bevor das automatische Layout angewendet wird. Die Codeausschnitte zeigen, wie Flussdiagrammlayouts und kompakte Baumlayouts angewendet werden.

**Die Quelle diagram.** 

![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_1.png)

Die Code-Snippets in diesem Artikel verwenden die Quelle diagram und wenden mehrere Arten von automatischem Layout darauf an, wobei sie jeweils in einer separaten Datei gespeichert werden.

|<p>**Layoutformen von unten nach oben** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layoutformen von oben nach unten** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Layoutformen von links nach rechts** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layoutformen von rechts nach links** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_5.png)</p>|
So gestalten Sie Formen im Flussdiagrammstil:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse und legen Sie die Eigenschaften für den Flussdiagrammstil fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnung Visio zu schreiben.
### **Programmierbeispiel im Flussdiagrammstil**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInFlowchartStyle.py" >}}
### **Anordnen von Formen im kompakten Baumstil**
Der kompakte Baumlayoutstil versucht, eine Baumstruktur aufzubauen. Es verwendet dieselbe Eingabedatei wie das obige Beispiel und speichert in mehreren verschiedenen kompakten Baumstilen.

|<p>**Kompaktes Baumlayout - unten und rechts** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Kompaktes Baumlayout - unten und links** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Kompaktes Baumlayout - rechts und unten** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Kompaktes Baumlayout - links und unten** </p><p>![todo: Bild_alt_Text](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Formen im kompakten Baumstil anordnen:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz der LayoutOptions-Klasse, und legen Sie kompakte Baumstileigenschaften fest.
1. Rufen Sie die Layout-Methode der Klasse Diagram auf, indem Sie LayoutOptions übergeben.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Datei Visio zu schreiben.
#### **Kompaktes Programmierbeispiel im Baumstil**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInCompactTreeStyle.py" >}}
## **Passen Sie die Visio Diagram automatisch an**
Aspose.Diagram API unterstützt die automatische Anpassung der Zeichnung Visio. Diese Feature-Operation hilft, äußere Formen innerhalb der Visio-Seitenbegrenzung zu bringen.

Aspose.Diagram for Python via Java API has the Diagram class that represents a Visio drawing. The DiagramSaveOptions class exposes AutoFitPageToDrawingContent property to auto fit the Visio drawing.

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Erstellen Sie ein Objekt der Klasse DiagramSaveOptions und übergeben Sie das resultierende Dateiformat.
1. Legen Sie die AutoFitPageToDrawingContent-Eigenschaft des DiagramSaveOptions-Objekts fest.
1. Rufen Sie die Save-Methode des Klassenobjekts Diagram auf und übergeben Sie auch den vollständigen Dateipfad und das DiagramSaveOptions-Objekt.
### **Programmierbeispiel für automatische Anpassung**
Der folgende Beispielcode zeigt, wie Formen in Visio diagram automatisch angepasst werden.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-AutoFitShapesInVisio.py" >}}
## **Arbeiten mit VBA-Projekt**
### **Ändern Sie den VBA-Modulcode in Visio Diagram**
This article demonstrates how to modify a VBA module code automatically using Aspose.Diagram for Python via Java.

Wir haben die Klassen VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference und VbaProjectReferenceCollection hinzugefügt. Diese Klassen helfen dabei, die Kontrolle über das VBA-Projekt zu erlangen. Entwickler können VBA-Modulcode extrahieren und ändern.
### **Programmierbeispiel für VBA-Modulcode ändern**
Bitte überprüfen Sie dieses Codebeispiel:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-ModifyVBAModuleCode.py" >}}
### **Entfernen Sie alle Makros aus Visio Diagram**
Aspose.Diagram for Python via Java allows developers to remove all macros from the Visio diagram.

Die JavaProjectData-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, ermöglicht es Ihnen, alle Makros aus der Visio-Zeichnung zu entfernen.
### **Programmierbeispiel für alle Makros entfernen**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-RemoveMacrosFromVisio.py" >}}
