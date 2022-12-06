---
title: Définition de cellules dans la section Événement de ShapeSheet
type: docs
weight: 10
url: /fr/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

À l'aide de Aspose.Diagram API, les développeurs peuvent définir comment une forme répond à des actions utilisateur spécifiques en écrivant des formules Visio qui gèrent automatiquement les événements. Chaque fois que l'utilisateur effectue l'une des actions décrites ci-dessous, la formule dans la cellule ShapeSheet correspondante est évaluée.

- **Le texte** - Un élément d'événement qui est évalué lorsque le texte ou la composition du texte d'une forme change.
- **EventXFMod** - La position, la taille ou l'orientation de la forme sur la page est modifiée.
- **ÉvénementDblClic** - La forme est double-cliquée.
- **EventDrop** Une nouvelle instance est créée en collant, en dupliquant ou en faisant glisser une forme, ou en faisant glisser et en déposant un maître.
- **ÉvénementMultiDrop** - lorsque plusieurs nouvelles instances sont créées en collant, en dupliquant ou en faisant glisser une forme, ou en faisant glisser et en déposant un maître.
- **Les données** - Réservé pour une utilisation future.

{{% /alert %}} 
## **Définition des cellules d'événement**
[Événement](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) permet aux développeurs de définir des cellules d'événement dans la feuille ShapeSheet. Cette rubrique d'aide montre comment les développeurs peuvent définir des formules dans les cellules d'événement :

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-eventsection-SettingEventCells-SettingEventCells.java" >}}
