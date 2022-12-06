---
title: Schützen Sie Formen in Visio
type: docs
weight: 20
url: /de/net/protect-shapes-in-visio/
---
Die Eigenschaften LockAspect, LockBegin, LockCalcWH, LockCrop, LockCustProp, LockDelete, LockEnd, LockFormat, LockFromGroupFormat, LockGroup, LockHeight, LockMoveX, LockMoveY, LockRotate, LockSelect, LockTextEdit, LockThemeColors, LockThemeEffects, LockVtxEdit und LockWidth, die von der Schutzklasse bereitgestellt werden, unterstützen das Objekt Aspose.Diagram.BoolValue . Diese Eigenschaften können verwendet werden, um Formen zu schützen/den Schutz aufzuheben.

In Visio müssen Sie die folgenden Aktionen ausführen, um eine beliebige Form zu schützen:

- Öffnen Sie diagram in MS Visio
- Wählen Sie eine beliebige Form aus
- Wählen Sie „Schutz…“ aus dem Menü „Format“, wenn Sie Visio 2007 verwenden, oder wählen Sie „Schutz“ aus dem Menü „Entwickler“, wenn Sie Visio 2010 verwenden
- Aktivieren/deaktivieren Sie im Fenster „Schutz“ ein beliebiges Textfeld, um Formattribute zu sperren oder zu entsperren
- Drücke OK'

Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um mit Aspose.Diagram for .NET dasselbe zu tun (beliebiges Formattribut zu sperren).

{{< highlight "csharp" >}}

 //Load diagram

Diagram diagram = new Diagram("ProtectShape.vsd");

Page page0 = diagram.Pages[0];

Shape shape = page0.Shapes[0];

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

diagram.Save("ProtectedShapesFile.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Beispielcode herunterladen**
- [Bit Bucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
