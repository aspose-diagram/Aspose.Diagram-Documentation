---
title: Utilizzo delle celle definite dall'utente
type: docs
weight: 100
url: /it/java/working-with-user-defined-cells/
---
## **Leggi celle definite dall'utente delle forme Visio**
 Gli utenti inseriscono campi di testo nelle forme per visualizzare informazioni aggiuntive.**Celle definite dall'utente** è l'unico ramo di questi campi e questo ramo utilizza le informazioni immesse nella cella Valore della sezione Celle definite dall'utente nello ShapeSheet della forma. Gli sviluppatori possono inserire e leggere tutte le celle definite dall'utente utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 La raccolta Users esposta da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) supporta l'oggetto com.aspose.diagram.User. Il[Utente](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) class può essere utilizzato per leggere le proprietà. Ci sono alcune celle definite dall'utente come puoi vedere nell'immagine seguente:

**Tabella che mostra le informazioni sulle celle definite dall'utente** 

![cose da fare:immagine_alt_testo](working-with-user-defined-cells_1.png)

Il codice seguente viene utilizzato per leggere le celle definite dall'utente.

L'immagine seguente mostra l'output dopo l'esecuzione del codice:

![cose da fare:immagine_alt_testo](working-with-user-defined-cells_2.png)
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.java" >}}
### **Crea cella definita dall'utente**
Il Aspose.Diagram for Java API consente agli sviluppatori di creare celle definite dall'utente nel foglio di forma. Questo argomento di esempio descrive come aggiungere tutte le righe del nome utente necessarie, assegnare nomi significativi alle righe e impostare i valori delle celle.

Il metodo add esposto dalla raccolta Users può essere utilizzato per creare una cella definita dall'utente nel foglio di forma. Ci vuole un solo parametro.

Utilizzare il seguente codice nell'applicazione Java per creare una cella definita dall'utente nel foglio di forma utilizzando Aspose.Diagram for Java.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
## **Recupera celle definite dall'utente da Shapesheet**
Aspose.Diagram for Java API consente agli sviluppatori di recuperare le celle definite dall'utente dal foglio di forma. Questo argomento di esempio descrive come recuperare tutti i nomi utente per tutte le forme in un disegno.
### **Recupera celle definite dall'utente**
 I metodi getNameU(), getValue().getVal() e getPrompt().getValue() esposti dal[Utente](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)class può essere utilizzata per recuperare le celle definite dall'utente dal foglio di forma.
#### **Recupera celle da esempi di programmazione di fogli di forma**
Utilizzare il seguente codice nell'applicazione Java per recuperare tutte le celle definite dall'utente dal foglio di forma utilizzando Aspose.Diagram for Java.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
