---
title: Utilizzo delle celle definite dall'utente
type: docs
weight: 150
url: /it/net/working-with-user-defined-cells/
description: Questa sezione spiega come leggere le celle definite dall'utente delle forme visio con Aspose.Diagram.
---
## **Leggi celle definite dall'utente delle forme Visio**
 Gli utenti inseriscono campi di testo nelle forme per visualizzare informazioni aggiuntive.**Celle definite dall'utente** è l'unico ramo di questi campi e questo ramo utilizza le informazioni immesse nella cella Valore della sezione Celle definite dall'utente nello ShapeSheet della forma. Gli sviluppatori possono inserire e leggere tutte le celle definite dall'utente utilizzando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Recupera i campi delle celle definiti dall'utente**
 Raccolta utenti esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class supporta l'oggetto Aspose.Diagram.User. Questa proprietà può essere utilizzata per leggere le celle definite dall'utente di una forma Visio disponibili nella sezione Celle definite dall'utente dello ShapeSheet della forma.

![cose da fare:immagine_alt_testo](working-with-user-defined-cells_1.png)
#### **Esempio di programmazione Recupera celle**
Il seguente pezzo di codice consente agli sviluppatori di leggere i campi delle celle definite dall'utente.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.cs" >}}


Questa immagine mostra l'output dopo aver eseguito il codice precedente:

![cose da fare:immagine_alt_testo](working-with-user-defined-cells_2.png)
## **Crea una cella definita dall'utente in ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) permette di creare celle definite dall'utente nel foglio di forma. Questo argomento di esempio descrive il modo in cui gli sviluppatori possono aggiungere tutte le righe User.name di cui hanno bisogno, assegnare nomi significativi alle righe e impostare i valori delle celle.
### **Crea cella definita dall'utente**
Il metodo Add esposto dalla raccolta Users può essere utilizzato per creare una cella definita dall'utente nel foglio di forma. Ci vuole un solo parametro.
#### **Crea un esempio di programmazione cellulare**
Utilizzare il seguente esempio di codice nell'applicazione .NET per creare una cella definita dall'utente nel foglio di forma utilizzando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.cs" >}}
## **Recupera celle definite dall'utente da Shapesheet**
Aspose.Diagram for .NET API consente di recuperare le celle definite dall'utente dal foglio di forma. Questo argomento di esempio descrive il modo in cui gli sviluppatori possono recuperare tutti gli User.name per tutte le forme in un disegno.
### **Recupera celle definite dall'utente**
Le proprietà NameU, Value.Val e Prompt.Value esposte dalla classe User possono essere utilizzate per recuperare le celle definite dall'utente dal foglio di forma.
#### **Recupera celle da esempi di programmazione di fogli di forma**
Utilizzare il seguente codice nell'applicazione .NET per recuperare tutte le celle definite dall'utente dal foglio di forma utilizzando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-RetrieveUserDefinedCells-RetrieveUserDefinedCells.cs" >}}
