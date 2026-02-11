---
title: Utilisation des en-têtes et pieds de page
type: docs
weight: 150
url: /fr/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java fournit un mécanisme pour définir les en-têtes et les pieds de page des diagrammes Microsoft Office Visio. Les développeurs peuvent obtenir ou définir la chaîne de texte qui apparaît à gauche, au centre et à droite d'un en-tête/pied de page de document. Ils peuvent également définir la marge d'en-tête et de pied de page ainsi que les propriétés de police du texte.

{{% /alert %}} 
### **Définition des propriétés des en-têtes et des pieds de page**
 La[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)L'objet de classe offre la propriété HeaderFooter qui permet d'obtenir et de définir les valeurs de texte, de police et de marge de l'en-tête et du pied de page. Lors de l'aperçu avant impression du dessin Visio, les utilisateurs peuvent cliquer sur le bouton de lien "Modifier l'en-tête et le pied de page" dans Microsoft Visio 2013 (dans Microsoft Visio 2010 >> bouton "En-tête et pied de page"). Il existe quelques options pour ajouter du texte, comme indiqué dans la capture d'écran ci-dessous. Les utilisateurs peuvent gérer ces propriétés par programmation en utilisant Aspose.Diagram API comme suit :

**Gérez le texte, les marges et les propriétés de police des en-têtes et des pieds de page.** 

![tâche : image_autre_texte](working-with-headers-and-footers_1.png)

Le morceau de code suivant permet de gérer les propriétés des en-têtes et des pieds de page.
#### **Exemples de programmation**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
