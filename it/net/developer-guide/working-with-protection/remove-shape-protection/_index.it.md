---
title: Rimuovi la protezione della forma
type: docs
weight: 20
url: /it/net/remove-shape-protection/
description: Questa sezione spiega come rimuovere la protezione della forma.
---
## **Rimuovere la protezione della forma Visio**
 La protezione delle forme Visio consente agli utenti di bloccare aspetti specifici delle forme. Gli aspetti delle forme che possono essere bloccati tramite la protezione delle forme includono larghezza, altezza, posizione x, posizione y, rotazione e altro. Gli sviluppatori possono raggiungere questo obiettivo utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Modifica la protezione della forma Visio**
**LockAspect**, **LockBegin**, **LockCalc WH**, **LockCrop**, **LockCustProp**, **BloccaElimina**, **LockEnd**, **BloccaFormat**, **LockFromGroupFormat**, **Gruppo di blocco**, **LockHeight**, **LockMoveX**, **LockMoveY**, **Blocca Ruota**, **BloccaSeleziona**, **LockTextModifica**, **LockThemeColors**, **LockThemeEffects**, **LockVtxModifica** e**LockWidth** proprietà esposte da[**Protezione**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) classe sostenere il**Aspose.Diagram.BoolValue** oggetto. Queste proprietà possono essere utilizzate per proteggere e rimuovere la protezione delle forme.

In Microsoft Office Visio, l'utente può eseguire le seguenti azioni per proteggere qualsiasi forma:

- Aperto diagram in Microsoft Office Visio
- Seleziona qualsiasi forma
- Selezionare 'Protezione' dal menu 'Formato' se si utilizza Visio 2007 o selezionare 'Protezione' dal menu 'Sviluppatore' se si utilizza Visio 2010
- Nella finestra "Protezione", deseleziona qualsiasi casella di testo per sbloccare qualsiasi attributo della forma
- Premere OK'
### **Rimuovi l'esempio di programmazione di Shape Protection**
Usa il seguente codice nella tua applicazione .NET per fare la stessa cosa (sbloccare qualsiasi attributo di forma) usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-RemoveShapeProtection-RemoveShapeProtection.cs" >}}
