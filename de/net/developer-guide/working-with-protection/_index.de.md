---
title: Arbeiten mit Schutz
type: docs
weight: 170
url: /de/net/working-with-protection/
description: In diesem Abschnitt wird erklärt, wie Sie die diagram mit Aspose.Diagram schützen.
---
## **Stellen Sie den Schutz der Visio Diagram ein**
 Durch das Schützen von Diagrammen können Benutzer Hintergründe, Vorlagen (Schablonen), Formen und Stile sperren, sodass sie nicht bearbeitet werden können. Dies ist beispielsweise nützlich, um Unternehmensstile zu schützen und ein konsistentes Erscheinungsbild über eine Reihe von Diagrammen hinweg sicherzustellen. Entwickler können dies mit erreichen[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Bearbeiten Sie den Visio Diagram Schutz**
Die Eigenschaften ProtectBkgnds, ProtectMasters, ProtectShapes und ProtectStyles, die von der[Dokumenteinstellungen](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) -Klasse unterstützt das Objekt Aspose.Diagram.BoolValue. Diese Eigenschaften können verwendet werden, um Microsoft Office Visio Diagramme zu schützen und den Schutz aufzuheben. In Microsoft Visio schützen Sie Dokumente auf diese Weise:

1. Öffnen Sie eine diagram in Microsoft Visio.
1. Öffnen Sie das Zeichnungs-Explorer-Fenster.
1.  Klicken Sie mit der rechten Maustaste auf eine diagram und wählen Sie sie aus**Dokument schützen** aus dem Menü.
1. Aktivieren oder deaktivieren Sie im Fenster Dokument schützen die Optionen zum Sperren oder Entsperren verschiedener diagram-Elemente.
1.  Klicken**OK**.
#### **Bearbeiten Sie das Diagram Protection Programming Sample**
Verwenden Sie den folgenden Code in einer .NET-Anwendung, um dieselben Aufgaben wie das Sperren und Entsperren verschiedener Elemente der Visio diagram mit Aspose.Diagram for .NET API auszuführen.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.DocumentSettings.ProtectBkgnds = BOOL.True;
diagram.DocumentSettings.ProtectMasters = BOOL.True;
diagram.DocumentSettings.ProtectShapes = BOOL.True;
diagram.DocumentSettings.ProtectStyles = BOOL.True;
// Save diagram
diagram.Save(dataDir + "VisioDiagramProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Stellen Sie den Schutz der Form Visio ein**
 Durch das Schützen von Visio-Formen können Benutzer bestimmte Aspekte von Formen sperren. Zu den Aspekten von Formen, die durch Formschutz gesperrt werden können, gehören Breite, Höhe, x-Position, y-Position, Rotation und mehr. Entwickler können dies mit erreichen[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Bearbeiten Sie den Formschutz Visio**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **SperrenLöschen**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **LockGroup**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LockRotate**, **LockSelect**, **LockTextEdit**, **Themenfarben sperren**, **LockThemeEffects**, **LockVtxBearbeiten** und**Sperrbreite** Eigenschaften ausgesetzt durch[**Schutz**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) Klasse unterstützt die**Aspose.Diagram.BoolValue** Objekt. Diese Eigenschaften können zum Schützen und Aufheben des Schutzes von Formen verwendet werden.

In Microsoft Office Visio kann der Benutzer die folgenden Aktionen ausführen, um jede Form zu schützen:

- Öffnen Sie diagram in Microsoft Office Visio
- Wählen Sie eine beliebige Form aus
- Wählen Sie „Schutz…“ aus dem Menü „Format“, wenn Sie Visio 2007 verwenden, oder wählen Sie „Schutz“ aus dem Menü „Entwickler“, wenn Sie Visio 2010 verwenden
- Aktivieren/deaktivieren Sie im Fenster „Schutz“ ein beliebiges Textfeld, um Formattribute zu sperren oder zu entsperren
- Drücke OK'
### **Bearbeiten Sie das Shape Protection-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um mit Aspose.Diagram for .NET dasselbe zu tun (beliebiges Formattribut sperren/entsperren).


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);

// Set protections
shape.Protection.LockAspect.Value = BOOL.True;
shape.Protection.LockBegin.Value = BOOL.True;
shape.Protection.LockCalcWH.Value = BOOL.True;
shape.Protection.LockCrop.Value = BOOL.True;
shape.Protection.LockCustProp.Value = BOOL.True;
shape.Protection.LockDelete.Value = BOOL.True;
shape.Protection.LockEnd.Value = BOOL.True;
shape.Protection.LockFormat.Value = BOOL.True;
shape.Protection.LockFromGroupFormat.Value = BOOL.True;
shape.Protection.LockGroup.Value = BOOL.True;
shape.Protection.LockHeight.Value = BOOL.True;
shape.Protection.LockMoveX.Value = BOOL.True;
shape.Protection.LockMoveY.Value = BOOL.True;
shape.Protection.LockRotate.Value = BOOL.True;
shape.Protection.LockSelect.Value = BOOL.True;
shape.Protection.LockTextEdit.Value = BOOL.True;
shape.Protection.LockThemeColors.Value = BOOL.True;
shape.Protection.LockThemeEffects.Value = BOOL.True;
shape.Protection.LockVtxEdit.Value = BOOL.True;
shape.Protection.LockWidth.Value = BOOL.True;
            
// Save diagram
diagram.Save(dataDir + "VisioShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

