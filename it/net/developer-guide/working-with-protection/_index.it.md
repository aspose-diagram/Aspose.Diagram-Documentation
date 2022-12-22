---
title: Lavorare con la protezione
type: docs
weight: 170
url: /it/net/working-with-protection/
description: Questa sezione spiega come impostare la protezione nello diagram con Aspose.Diagram.
---
## **Set Protezione del Visio Diagram**
 La protezione dei diagrammi consente agli utenti di bloccare sfondi, master (stencil), forme e stili in modo che non possano essere modificati. Ciò è utile per proteggere gli stili aziendali, ad esempio, e garantire un aspetto coerente in una serie di diagrammi. Gli sviluppatori possono raggiungere questo obiettivo utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Modifica la protezione Visio Diagram**
Le proprietà ProtectBkgnds, ProtectMasters, ProtectShapes e ProtectStyles, esposte da[Impostazioni documento](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) class supporta l'oggetto Aspose.Diagram.BoolValue. Queste proprietà possono essere utilizzate per proteggere e sproteggere i diagrammi Microsoft Office Visio. In Microsoft Visio proteggi i documenti in questo modo:

1. Apri uno diagram in Microsoft Visio.
1. Apre la finestra Esplora Disegno.
1.  Fare clic con il tasto destro su diagram e selezionare**Proteggi documento** dal menù.
1. Nella finestra Proteggi documento, seleziona o deseleziona le opzioni per bloccare o sbloccare diversi elementi diagram.
1.  Clic**OK**.
#### **Modificare l'esempio di programmazione della protezione Diagram**
Utilizzare il codice seguente in un'applicazione .NET per eseguire le stesse attività come bloccare e sbloccare diversi elementi di Visio diagram utilizzando Aspose.Diagram for .NET API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioDiagramProtection-VisioDiagramProtection.cs" >}}
## **Set Protezione della Forma Visio**
 La protezione delle forme Visio consente agli utenti di bloccare aspetti specifici delle forme. Gli aspetti delle forme che possono essere bloccati tramite la protezione delle forme includono larghezza, altezza, posizione x, posizione y, rotazione e altro. Gli sviluppatori possono raggiungere questo obiettivo utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Modifica la protezione della forma Visio**
**LockAspect**, **LockBegin**, **LockCalc WH**, **LockCrop**, **LockCustProp**, **BloccaElimina**, **LockEnd**, **BloccaFormat**, **LockFromGroupFormat**, **Gruppo di blocco**, **LockHeight**, **LockMoveX**, **LockMoveY**, **Blocca Ruota**, **BloccaSeleziona**, **LockTextModifica**, **LockThemeColors**, **LockThemeEffects**, **LockVtxModifica** e**LockWidth** proprietà esposte da[**Protezione**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) classe sostenere il**Aspose.Diagram.BoolValue** oggetto. Queste proprietà possono essere utilizzate per proteggere e rimuovere la protezione delle forme.

In Microsoft Office Visio, l'utente può eseguire le seguenti azioni per proteggere qualsiasi forma:

- Aperto diagram in Microsoft Office Visio
- Seleziona qualsiasi forma
- Seleziona 'Protezione…' dal menu 'Formato' se stai usando Visio 2007 o seleziona 'Protezione' dal menu 'Sviluppatore' se stai usando Visio 2010
- Nella finestra "Protezione", seleziona/deseleziona qualsiasi casella di testo per bloccare o sbloccare qualsiasi attributo della forma
- Premere OK'
### **Modifica l'esempio di programmazione di Shape Protection**
Usa il seguente codice nella tua applicazione .NET per fare la stessa cosa (bloccare/sbloccare qualsiasi attributo di forma) usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioShapeProtection-VisioShapeProtection.cs" >}}
