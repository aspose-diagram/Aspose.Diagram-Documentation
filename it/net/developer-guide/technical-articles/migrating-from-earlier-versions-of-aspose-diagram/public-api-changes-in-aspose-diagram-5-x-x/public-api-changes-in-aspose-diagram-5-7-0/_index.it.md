---
title: Pubblico API Modifiche Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /it/net/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 5.6.0 alla 5.7.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **Imposta le stringhe del modello di data sulla linea temporale**
Le nuove proprietà DateFormatStringForBE e DateFormatStringForIntm sono state aggiunte nella classe TimelineHelper. Esempi di codici:

**C#**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd";

// set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd";

{{< /highlight >}}

**V.B**

{{< highlight "java" >}}

 ' set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd"

' set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd"

{{< /highlight >}}
