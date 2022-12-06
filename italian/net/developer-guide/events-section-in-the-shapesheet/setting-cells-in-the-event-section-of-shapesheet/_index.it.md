---
title: Impostazione delle celle nella sezione Event di ShapeSheet
type: docs
weight: 10
url: /it/net/setting-cells-in-the-event-section-of-shapesheet/
description: Gestisci le proprietà degli eventi dei file visio.
---
{{% alert color="primary" %}} 

Utilizzando Aspose.Diagram API, gli sviluppatori possono definire in che modo una forma risponde a specifiche azioni dell'utente scrivendo formule Visio che gestiscono automaticamente gli eventi. Ogni volta che l'utente esegue una delle quattro azioni descritte di seguito, viene valutata la formula nella cella ShapeSheet corrispondente.

- **Il testo** - Un elemento evento che viene valutato quando il testo di una forma o la composizione del testo cambiano.
- **EventoXFMod** - La posizione, le dimensioni o l'orientamento della forma sulla pagina viene modificata.
- **EventDblClick** - Si fa doppio clic sulla forma.
- **EventDrop** Una nuova istanza viene creata incollando, duplicando o trascinando una forma o trascinando e rilasciando un master.
- **EventoMultiDrop** - quando vengono create più nuove istanze incollando, duplicando o trascinando una forma o trascinando e rilasciando un master.
- **I dati** - Riservato per uso futuro.

{{% /alert %}} 
## **Impostazione delle celle degli eventi**
[Evento](https://reference.aspose.com/diagram/net/aspose.diagram/event) class consente agli sviluppatori di impostare le celle degli eventi in ShapeSheet. Questo argomento della guida mostra come gli sviluppatori possono impostare le formule nelle celle degli eventi:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Event-Section-SettingCellsInEventSection-SettingCellsInEventSection.cs" >}}
