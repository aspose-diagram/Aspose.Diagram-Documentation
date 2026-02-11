---
title: Insérez un contrôle ActiveX dans le Visio Diagram
type: docs
weight: 10
url: /fr/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 Les développeurs peuvent ajouter des contrôles ActiveX directement aux dessins Microsoft Visio pour rendre le Visio diagram interactif en utilisant[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Insérer un exemple de programmation de contrôle ActiveX**
[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) La classe offre la méthode addActiveXControl et permet aux développeurs d'insérer n'importe quel type de contrôle ActiveX comme le bouton de commande, la liste déroulante, la case à cocher, la liste, la zone de texte, le bouton rotatif, le bouton radio, l'étiquette, l'image, le bouton bascule et la barre de défilement.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertanActiveControl.class) + "VisioActiveXControls/";
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);
// Save diagram
diagram.save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

