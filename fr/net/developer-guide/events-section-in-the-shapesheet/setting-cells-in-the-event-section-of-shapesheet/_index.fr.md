---
title: Définition de cellules dans la section Événement de ShapeSheet
type: docs
weight: 10
url: /fr/net/setting-cells-in-the-event-section-of-shapesheet/
description: Gérer les propriétés d'événement des fichiers visio.
---
{{% alert color="primary" %}} 

À l'aide de Aspose.Diagram API, les développeurs peuvent définir comment une forme répond à des actions utilisateur spécifiques en écrivant des formules Visio qui gèrent automatiquement les événements. Chaque fois que l'utilisateur effectue l'une des quatre actions décrites ci-dessous, la formule dans la cellule ShapeSheet correspondante est évaluée.

- **Le texte** - Un élément d'événement qui est évalué lorsque le texte ou la composition du texte d'une forme change.
- **EventXFMod** - La position, la taille ou l'orientation de la forme sur la page est modifiée.
- **ÉvénementDblClic** - La forme est double-cliquée.
- **EventDrop** Une nouvelle instance est créée en collant, en dupliquant ou en faisant glisser une forme, ou en faisant glisser et en déposant un maître.
- **ÉvénementMultiDrop** - lorsque plusieurs nouvelles instances sont créées en collant, en dupliquant ou en faisant glisser une forme, ou en faisant glisser et en déposant un maître.
- **Les données** - Réservé pour une utilisation future.

{{% /alert %}} 
## **Définition des cellules d'événement**
[Événement](https://reference.aspose.com/diagram/net/aspose.diagram/event) permet aux développeurs de définir des cellules d'événement dans la feuille ShapeSheet. Cette rubrique d'aide montre comment les développeurs peuvent définir des formules dans les cellules d'événement :

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Event-Section-SettingCellsInEventSection-SettingCellsInEventSection.cs" >}}
