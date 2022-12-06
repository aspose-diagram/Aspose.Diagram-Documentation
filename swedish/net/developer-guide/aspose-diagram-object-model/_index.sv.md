---
title: Aspose.Diagram Objektmodell
linktitle: Aspose.Diagram Objektmodell
type: docs
description: Aspose.Diagram Objektmodell ger information om de strukturella relationerna mellan objekten i Aspose.Diagram klassbibliotek.
weight: 20
url: /sv/net/object_model
---
{{% alert color="primary" %}} 

**Aspose.Diagram Objektmodell**

Aspose.Diagram Objektmodell ger information om de strukturella relationerna mellan objekten i Aspose.Diagram klassbibliotek.

{{% /alert %}} 

### Den översta nivåstrukturen för objektmodellen Aspose.Diagram visas nedan på ett hierarkiskt sätt.

|**Struktur på översta nivån för Aspose.Diagram Objektmodell**|
|:- |
|![Struktur på översta nivån för Aspose.Diagram Objektmodell](diagram-classes.png)|

Som du kan se från ovanstående figur är roten av objektmodellen objektet Diagram. En kort beskrivning av några av objekten ges nedan i introduktionssyfte.

#### **Sidsamling/sida**

Diagram-objektet innehåller PageCollection, som representerar samlingen av alla sidobjekt i ett Diagram.

#### **ShapeCollection/Shape**

Sidobjektet innehåller ShapeCollection, som representerar samlingen av alla Shape-objekt på en sida. Shape-objekt innehåller element som definierar en form i ett huvud-, sida- eller gruppformelement.

#### **ConnectCollection/Connect**

Sidobjektet innehåller ConnectCollection, som representerar samlingen av alla Connect-objekt på en sida. Connect-objekt representerar en koppling mellan två former i en ritning, till exempel en linje och en ruta i ett organisationsschema.

#### **StyleSheet Collection/StyleSheet**

Representerar en stil som definieras i ett dokument.

#### **MasterCollection/Master**

Innehåller element som definierar en mall för dokumentet. En master är en form på en stencil som du använder upprepade gånger för att skapa ritningar. När du drar en form från en stencil till ritsidan blir formen en instans av den mallen och en lokal kopia av mallen ingår i dokumentet.

#### **Dokument egenskaper**

Innehåller dokumentegenskapselement som dokumentets titel, författare och så vidare.

#### **Sidhuvud**

Innehåller element för ett dokuments sidhuvud och sidfot.

#### **VbaProject**

Representerar VBA-projektet.

#### **Temasamling/tema**

Dynamiskt tema definierar egenskaper som anger egenskaper för färg, teckensnitt, fyllning, linjeegenskaper och effekt.

#### **Fylla**

Innehåller de aktuella fyllningsformateringsvärdena för formen och formens skugga, inklusive mönster, förgrundsfärg och bakgrundsfärg.

#### **Linje**

Innehåller element som styr linjeattribut för en form, såsom mönster, vikt och färg. Dessa element bestämmer om linjeändarna är formaterade (till exempel med en pilspets), storleken på linjeslutsformaten, radien för den avrundade cirkeln som tillämpas på linjen och linjekapselstilen (rund eller fyrkantig).

#### **Geoms**

Innehåller en samling Geom-element.

#### **Tecken**

Innehåller en samling Char-objekt som innehåller formens textstilar.

#### **Text**

Innehåller texten till en form.

#### **XForm**

Innehåller element som anger allmän positioneringsinformation om en form.

#### **TextXForm**

Innehåller element som anger positionsinformation om en forms textblock.

#### **HyperlinkCollection/Hyperlink**

Hyperlänkobjekt innehåller element för att skapa flera hopp mellan en form- eller ritsida och en annan ritsida, en annan fil eller en webbplats.

#### **MasterShape**

Det här attributet får bara finnas i former som är medlemmar i en gruppform, och gruppen är en instans av en master. Attributet innehåller ett ID som refererar till motsvarande underform i mastern.

#### **Fältsamling/fält**

Fältobjekt innehåller element som anger funktioner och formler infogade i formens text.
