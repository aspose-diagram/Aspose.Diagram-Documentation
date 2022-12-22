---
title: Lavorare con i livelli
type: docs
weight: 160
url: /it/java/working-with-layers/
---
### **Configurazione di oggetti forma con livelli**
Aspose.Diagram for Java consente di configurare oggetti forma con livelli in Microsoft Office Visio diagram. Ogni forma può appartenere a più livelli in modo che gli sviluppatori possano gestire le forme in base alle esigenze dell'utente finale.

 Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) L'oggetto class offre la proprietà LayerMember che consente di aggiungere/rimuovere oggetti forma a/dai livelli nel disegno Visio. Gli utenti possono gestire queste proprietà a livello di codice utilizzando Aspose.Diagram API come segue:

**Aggiungi, rimuovi e sposta oggetti forma a/da livelli di diagram.** 

![cose da fare:immagine_alt_testo](working-with-layers_1.png)

Il seguente pezzo di codice aiuta ad aggiungere, rimuovere e spostare le proprietà degli oggetti forma.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-ConfigureShapeLayers-ConfigureShapeLayers.java" >}}
### **Aggiungi un livello nel foglio di pagina Visio**
Aspose.Diagram for Java consente agli sviluppatori di aggiungere nuovi livelli per organizzare categorie personalizzate di forme e quindi assegnare forme a tali livelli in modo programmatico.

 Il[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class offre il metodo add che consente di aggiungere un nuovo file[Strato](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)oggetto di classe nel disegno Visio. Gli sviluppatori possono impostare le proprietà del livello inizializzando il suo oggetto di classe.

Il seguente pezzo di codice aiuta ad aggiungere oggetti Layer.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-AddLayer-AddLayer.java" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Java offre agli sviluppatori l'accesso ai livelli esistenti di Visio diagram.

{{% /alert %}} 
### **Ottieni tutti i livelli disponibili**
 Il[PaginaFoglio](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) proprietà del[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class consente di recuperare l'elenco dei livelli disponibili dal Visio diagram utilizzando[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) classe.

Il seguente pezzo di codice aiuta a ottenere l'elenco dei livelli.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-RetrieveAllLayers-RetrieveAllLayers.java" >}}
