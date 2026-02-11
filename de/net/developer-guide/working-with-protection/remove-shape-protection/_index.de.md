---
title: Formschutz entfernen
type: docs
weight: 20
url: /de/net/remove-shape-protection/
description: In diesem Abschnitt wird erläutert, wie Sie den Formschutz entfernen.
---
## **Entfernen Sie den Schutz der Form Visio**
 Durch das Schützen von Visio-Formen können Benutzer bestimmte Aspekte von Formen sperren. Zu den Aspekten von Formen, die durch Formschutz gesperrt werden können, gehören Breite, Höhe, x-Position, y-Position, Rotation und mehr. Entwickler können dies mit erreichen[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Bearbeiten Sie den Formschutz Visio**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **SperrenLöschen**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **LockGroup**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LockRotate**, **LockSelect**, **LockTextEdit**, **Themenfarben sperren**, **LockThemeEffects**, **LockVtxBearbeiten** und**Sperrbreite** Eigenschaften ausgesetzt durch[**Schutz**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) Klasse unterstützt die**Aspose.Diagram.BoolValue** Objekt. Diese Eigenschaften können zum Schützen und Aufheben des Schutzes von Formen verwendet werden.

In Microsoft Office Visio kann der Benutzer die folgenden Aktionen ausführen, um jede Form zu schützen:

- Öffnen Sie diagram in Microsoft Office Visio
- Wählen Sie eine beliebige Form aus
- Wählen Sie „Schutz“ aus dem Menü „Format“, wenn Sie Visio 2007 verwenden, oder wählen Sie „Schutz“ aus dem Menü „Entwickler“, wenn Sie Visio 2010 verwenden
- Deaktivieren Sie im Fenster „Schutz“ alle Textfelder, um Formattribute zu entsperren
- Drücke OK'
### **Entfernen Sie das Shape Protection-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um mit Aspose.Diagram for .NET dasselbe zu tun (entsperren Sie ein beliebiges Formattribut).

```
{{< highlight "csharp" >}}
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
shape.Protection.LockAspect.Value = BOOL.False;
shape.Protection.LockBegin.Value = BOOL.False;
shape.Protection.LockCalcWH.Value = BOOL.False;
shape.Protection.LockCrop.Value = BOOL.False;
shape.Protection.LockCustProp.Value = BOOL.False;
shape.Protection.LockDelete.Value = BOOL.False;
shape.Protection.LockEnd.Value = BOOL.False;
shape.Protection.LockFormat.Value = BOOL.False;
shape.Protection.LockFromGroupFormat.Value = BOOL.False;
shape.Protection.LockGroup.Value = BOOL.False;
shape.Protection.LockHeight.Value = BOOL.False;
shape.Protection.LockMoveX.Value = BOOL.False;
shape.Protection.LockMoveY.Value = BOOL.False;
shape.Protection.LockRotate.Value = BOOL.False;
shape.Protection.LockSelect.Value = BOOL.False;
shape.Protection.LockTextEdit.Value = BOOL.False;
shape.Protection.LockThemeColors.Value = BOOL.False;
shape.Protection.LockThemeEffects.Value = BOOL.False;
shape.Protection.LockVtxEdit.Value = BOOL.False;
shape.Protection.LockWidth.Value = BOOL.False;
            
// Save diagram
diagram.Save(dataDir + "RemoveShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
