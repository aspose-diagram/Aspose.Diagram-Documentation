---
title: Rimuovi la protezione della forma
type: docs
weight: 20
url: /it/python-java/remove-shape-protection/
description: This section explains how to remove shape protection using Aspose.Diagram for Python via Java.
---
## **Rimuovere la protezione della forma Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.
### **Modifica la protezione della forma Visio**
**LockAspect**, **LockBegin**, **LockCalc WH**, **LockCrop**, **LockCustProp**, **BloccaElimina**, **LockEnd**, **BloccaFormat**, **LockFromGroupFormat**, **Gruppo di blocco**, **LockHeight**, **LockMoveX**, **LockMoveY**, **Blocca Ruota**, **BloccaSeleziona**, **LockTextModifica**, **LockThemeColors**, **LockThemeEffects**, **LockVtxModifica** e**LockWidth** proprietà esposte da**Protezione** classe sostenere il**Aspose.Diagram.BoolValue** oggetto. Queste proprietà possono essere utilizzate per proteggere e rimuovere la protezione delle forme.

In Microsoft Office Visio, l'utente può eseguire le seguenti azioni per proteggere qualsiasi forma:

- Aperto diagram in Microsoft Office Visio
- Seleziona qualsiasi forma
- Selezionare 'Protezione' dal menu 'Formato' se si utilizza Visio 2007 o selezionare 'Protezione' dal menu 'Sviluppatore' se si utilizza Visio 2010
- Nella finestra "Protezione", deseleziona qualsiasi casella di testo per sbloccare qualsiasi attributo della forma
- Premere OK'

### **Rimuovi l'esempio di programmazione di Shape Protection**
Use the following code in your application to do the same thing (unlock any shape attribute) using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-RemoveShapeProtection.py" >}}

