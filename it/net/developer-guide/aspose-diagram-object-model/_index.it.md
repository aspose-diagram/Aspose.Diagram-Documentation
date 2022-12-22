---
title: Aspose.Diagram Modello oggetto
linktitle: Aspose.Diagram Modello oggetto
type: docs
description: Aspose.Diagram Object Model fornisce informazioni sulle relazioni strutturali tra gli oggetti della libreria di classi Aspose.Diagram.
weight: 20
url: /it/net/object_model
---
{{% alert color="primary" %}} 

**Aspose.Diagram Modello oggetto**

Aspose.Diagram Object Model fornisce informazioni sulle relazioni strutturali tra gli oggetti della libreria di classi Aspose.Diagram.

{{% /alert %}} 

### La struttura di livello superiore del modello a oggetti Aspose.Diagram è mostrata di seguito in modo gerarchico.

|**Struttura di primo livello del modello a oggetti Aspose.Diagram**|
|:- |
|![Struttura di primo livello del modello a oggetti Aspose.Diagram](diagram-classes.png)|

Come puoi vedere dalla figura sopra, la radice del modello a oggetti è l'oggetto Diagram. Di seguito viene fornita una breve descrizione di alcuni degli oggetti a scopo introduttivo.

#### **PaginaCollezione/Pagina**

Diagram contiene l'oggetto PageCollection, che rappresenta la raccolta di tutti gli oggetti Page in un oggetto Diagram.

#### **ShapeCollection/Shape**

L'oggetto Page contiene ShapeCollection, che rappresenta la raccolta di tutti gli oggetti Shape in un Page . L'oggetto forma contiene elementi che definiscono una forma in un elemento forma master, pagina o gruppo.

#### **ConnettiCollezione/Connetti**

L'oggetto Page contiene ConnectCollection, che rappresenta la raccolta di tutti gli oggetti Connect in un Page . L'oggetto Connect rappresenta una connessione tra due forme in un disegno, ad esempio una linea e una casella in un organigramma.

#### **Raccolta di fogli di stile/Fogli di stile**

Rappresenta uno stile definito in un documento.

#### **MasterCollezione/Master**

Contiene elementi che definiscono un master per il documento. Un master è una forma su uno stencil che usi ripetutamente per creare disegni. Quando trascini una forma da uno stencil nella pagina di disegno, la forma diventa un'istanza di tale master e una copia locale del master viene inclusa nel documento.

#### **Proprietà documento**

Contiene elementi di proprietà del documento come il titolo del documento, l'autore e così via.

#### **IntestazionePiè di pagina**

Contiene elementi per l'intestazione e il piè di pagina di un documento.

#### **VbaProject**

Rappresenta il progetto VBA.

#### **TemaCollezione/Tema**

Il tema dinamico definisce le proprietà che specificano le proprietà per il colore, il carattere, il riempimento, le proprietà della linea e l'effetto.

#### **Riempire**

Contiene i valori di formattazione del riempimento correnti per la forma e l'ombreggiatura della forma, inclusi motivo, colore di primo piano e colore di sfondo.

#### **Linea**

Contiene elementi che controllano gli attributi della linea per una forma, come motivo, spessore e colore. Questi elementi determinano se le estremità della linea sono formattate (ad esempio, con una punta di freccia), la dimensione dei formati delle estremità della linea, il raggio del cerchio di arrotondamento applicato alla linea e lo stile del capolinea (rotondo o quadrato).

#### **Geom**

Contiene una raccolta di elementi Geom.

#### **Caratteri**

Contiene una raccolta di oggetti Char che contiene gli stili di testo della forma.

#### **Testo**

Contiene il testo di una forma.

#### **XForm**

Contiene elementi che specificano informazioni di posizionamento generali su una forma.

#### **TestoXForm**

Contiene elementi che specificano le informazioni di posizionamento sul blocco di testo di una forma.

#### **Collegamento ipertestuale/collegamento ipertestuale**

L'oggetto collegamento ipertestuale contiene elementi per la creazione di più collegamenti tra una forma o una pagina di disegno e un'altra pagina di disegno, un altro file o un sito Web.

#### **MasterShape**

Questo attributo può essere presente solo nelle forme che sono membri di una forma di gruppo e il gruppo è un'istanza di un master. L'attributo contiene un ID che fa riferimento alla sottoforma corrispondente nel master.

#### **CampoCollezione/Campo**

L'oggetto Campo contiene elementi che specificano funzioni e formule inserite nel testo della forma.
