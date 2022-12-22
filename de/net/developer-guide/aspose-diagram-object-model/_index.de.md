---
title: Aspose.Diagram Objektmodell
linktitle: Aspose.Diagram Objektmodell
type: docs
description: Das Aspose.Diagram-Objektmodell gibt Auskunft über die strukturellen Beziehungen zwischen den Objekten der Aspose.Diagram-Klassenbibliothek.
weight: 20
url: /de/net/object_model
---
{{% alert color="primary" %}} 

**Aspose.Diagram Objektmodell**

Das Aspose.Diagram-Objektmodell gibt Auskunft über die strukturellen Beziehungen zwischen den Objekten der Aspose.Diagram-Klassenbibliothek.

{{% /alert %}} 

### Die Top-Level-Struktur des Objektmodells Aspose.Diagram ist unten hierarchisch dargestellt.

|**Top-Level-Struktur des Objektmodells Aspose.Diagram**|
|:- |
|![Top-Level-Struktur des Objektmodells Aspose.Diagram](diagram-classes.png)|

Wie Sie der obigen Abbildung entnehmen können, ist die Wurzel des Objektmodells das Objekt Diagram. Eine kurze Beschreibung einiger der Objekte wird unten für einführende Zwecke bereitgestellt.

#### **Seitensammlung/Seite**

Diagram-Objekt enthält die PageCollection, die die Auflistung aller Page-Objekte in einem Diagram darstellt.

#### **ShapeCollection/Form**

Das Page-Objekt enthält die ShapeCollection, die die Auflistung aller Shape-Objekte in einer Page darstellt. Shape-Objekt enthält Elemente, die eine Form in einem Master-, Seiten- oder Gruppen-Shape-Element definieren.

#### **ConnectCollection/Verbinden**

Das Page-Objekt enthält die ConnectCollection, die die Auflistung aller Connect-Objekte in einer Page darstellt. Das Verbindungsobjekt stellt eine Verbindung zwischen zwei Formen in einer Zeichnung dar, z. B. eine Linie und ein Feld in einem Organigramm.

#### **StyleSheetCollection/StyleSheet**

Stellt einen in einem Dokument definierten Stil dar.

#### **MasterCollection/Master**

Enthält Elemente, die einen Master für das Dokument definieren. Ein Master ist eine Form auf einer Schablone, die Sie wiederholt verwenden, um Zeichnungen zu erstellen. Wenn Sie ein Shape aus einer Schablone auf das Zeichenblatt ziehen, wird das Shape zu einer Instanz dieses Masters, und eine lokale Kopie des Masters wird in das Dokument aufgenommen.

#### **Dokumenteigenschaften**

Enthält Dokumenteigenschaftselemente wie Titel, Autor usw. des Dokuments.

#### **Kopfzeile Fußzeile**

Enthält Elemente für die Kopf- und Fußzeile eines Dokuments.

#### **VbaProjekt**

Stellt das VBA-Projekt dar.

#### **ThemeCollection/Thema**

Dynamisches Design definiert Eigenschaften, die Eigenschaften für Farbe, Schriftart, Füllung, Linieneigenschaften und Effekte angeben.

#### **Füllen**

Enthält die aktuellen Füllformatierungswerte für die Form und den Schlagschatten der Form, einschließlich Muster, Vordergrundfarbe und Hintergrundfarbe.

#### **Linie**

Enthält Elemente, die Linienattribute für eine Form steuern, z. B. Muster, Stärke und Farbe. Diese Elemente bestimmen, ob die Linienenden formatiert sind (z. B. mit einer Pfeilspitze), die Größe der Linienendeformate, den Radius des Rundungskreises, der auf die Linie angewendet wird, und den Linienabschlussstil (rund oder quadratisch).

#### **Geomen**

Enthält eine Sammlung von Geom-Elementen.

#### **Zeichen**

Enthält eine Sammlung von Char-Objekten, die Textstile der Form enthalten.

#### **Text**

Enthält den Text einer Form.

#### **XForm**

Enthält Elemente, die allgemeine Positionierungsinformationen zu einer Form angeben.

#### **TextXForm**

Enthält Elemente, die Positionierungsinformationen über den Textblock einer Form angeben.

#### **HyperlinkCollection/Hyperlink**

Das Hyperlink-Objekt enthält Elemente zum Erstellen mehrerer Sprünge zwischen einer Form oder einem Zeichenblatt und einem anderen Zeichenblatt, einer anderen Datei oder einer Website.

#### **MasterShape**

Dieses Attribut darf nur in Shapes vorhanden sein, die Mitglieder eines Gruppen-Shapes sind, und die Gruppe ist eine Instanz eines Masters. Das Attribut enthält eine ID, die auf die entsprechende Unterform im Master verweist.

#### **FieldCollection/Feld**

Das Field-Objekt enthält Elemente, die Funktionen und Formeln angeben, die in den Text der Form eingefügt werden.
