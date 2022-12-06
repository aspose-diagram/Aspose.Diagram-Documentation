---
title: Lavorare con i livelli
type: docs
weight: 160
url: /it/python-java/working-with-layers/
---
### **Configurazione di oggetti forma con livelli**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

 Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) L'oggetto class offre la proprietà LayerMember che consente di aggiungere/rimuovere oggetti forma a/dai livelli nel disegno Visio. Gli utenti possono gestire queste proprietà a livello di codice utilizzando Aspose.Diagram API come segue:

**Aggiungi, rimuovi e sposta oggetti forma a/da livelli di diagram.** 

Il seguente pezzo di codice aiuta ad aggiungere, rimuovere e spostare le proprietà degli oggetti forma.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **Aggiungi un livello nel foglio di pagina Visio**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

 Il[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class offre il metodo add che consente di aggiungere un nuovo file[Strato](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) oggetto di classe in[il disegno Visio](DrawingFlowChart.vsdx). Gli sviluppatori possono impostare le proprietà del livello inizializzando il suo oggetto di classe.

Il seguente pezzo di codice aiuta ad aggiungere oggetti Layer.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Python via Java gives developers access to the existing layers of Visio diagram.

{{% /alert %}} 
### **Ottieni tutti i livelli disponibili**
 Il[PaginaFoglio](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) proprietà del[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class consente di recuperare l'elenco dei layer disponibili da[il disegno Visio](DrawingFlowChart.vsdx) utilizzando[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) classe.

Il seguente pezzo di codice aiuta a ottenere l'elenco dei livelli.
#### **Esempi di programmazione**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}
