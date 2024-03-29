﻿---
title: Proteggi le forme in Visio
type: docs
weight: 20
url: /it/net/protect-shapes-in-visio/
---
Le proprietà LockAspect, LockBegin, LockCalcWH, LockCrop, LockCustProp, LockDelete, LockEnd, LockFormat, LockFromGroupFormat, LockGroup, LockHeight, LockMoveX, LockMoveY, LockRotate, LockSelect, LockTextEdit, LockThemeColors, LockThemeEffects, LockVtxEdit e LockWidth esposte dalla classe Protection supportano l'oggetto Aspose.Diagram.BoolValue . Queste proprietà possono essere utilizzate per proteggere/sproteggere le forme.

In Visio, è necessario eseguire le seguenti azioni per proteggere qualsiasi forma:

- Apri diagram in MS Visio
- Seleziona qualsiasi forma
- Seleziona 'Protezione…' dal menu 'Formato' se stai usando Visio 2007 o seleziona 'Protezione' dal menu 'Sviluppatore' se stai usando Visio 2010
- Nella finestra "Protezione", seleziona/deseleziona qualsiasi casella di testo per bloccare o sbloccare qualsiasi attributo della forma
- Premere OK'

Usa il seguente codice nella tua applicazione .NET per fare la stessa cosa (bloccare qualsiasi attributo di forma) usando Aspose.Diagram for .NET.

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
## **Scarica il codice di esempio**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
