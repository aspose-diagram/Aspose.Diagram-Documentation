---
title: Utilisation des en-têtes et pieds de page
type: docs
weight: 140
url: /fr/net/working-with-headers-and-footers/
description: Cette section explique comment définir les en-têtes et les pieds de page du Microsoft Office Visio avec Aspose.Diagram.
---
## **Gérer les en-têtes et pieds de page des diagrammes Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) fournit un mécanisme pour définir les en-têtes et les pieds de page des diagrammes Microsoft Office Visio. Les développeurs peuvent obtenir ou définir la chaîne de texte qui apparaît à gauche, au centre et à droite d'un en-tête/pied de page de document. Ils peuvent également définir la marge d'en-tête et de pied de page ainsi que les propriétés de police du texte.
### **Définition des propriétés des en-têtes et des pieds de page**
 La[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)L'objet de classe offre la propriété HeaderFooter qui permet d'obtenir et de définir les valeurs de texte, de police et de marge de l'en-tête et du pied de page. Lors de l'aperçu avant impression du dessin Visio, les utilisateurs peuvent cliquer sur le bouton de lien "Modifier l'en-tête et le pied de page" dans Microsoft Visio 2013 (dans Microsoft Visio 2010 >> bouton "En-tête et pied de page"). Il existe quelques options pour ajouter du texte, comme indiqué dans la capture d'écran ci-dessous. Les utilisateurs peuvent gérer ces propriétés par programmation en utilisant Aspose.Diagram API comme suit :
#### **Exemple de programmation**
Le morceau de code suivant permet de gérer les propriétés des en-têtes et des pieds de page.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
