---
title: Aspose.Diagram for .NET 6.3.0 Notes de mise à jour
type: docs
weight: 90
url: /fr/net/aspose-diagram-for-net-6-3-0-release-notes/
---
## **Autres améliorations et changements**

|**Clé** |**Sommaire** |**Catégorie** |
|:- |:- |:- |
|DIAGRAMNET-50739 | Ajout de la prise en charge de la détection du type Visio diagram.| Nouvelle fonctionnalité|
|DIAGRAMNET-50746 | Empêcher l'exportation des pages Visio masquées dans le PDF.| Nouvelle fonctionnalité|
|DIAGRAMNET-50747 | Empêcher l'exportation des pages Visio masquées dans le HTML.| Nouvelle fonctionnalité|
|DIAGRAMNET-50750 | Empêcher l'exportation des pages Visio masquées au format PNG.| Nouvelle fonctionnalité|
|DIAGRAMNET-50751 | Empêcher l'exportation des pages Visio masquées au format JPEG.| Nouvelle fonctionnalité|
|DIAGRAMNET-50752 | Empêcher l'exportation des pages Visio cachées dans le SVG.| Nouvelle fonctionnalité|
|DIAGRAMNET-50753 | Empêcher l'exportation des pages Visio masquées dans le GIF.| Nouvelle fonctionnalité|
|DIAGRAMNET-50754 | Empêcher l'exportation des pages Visio masquées dans le XPS.| Nouvelle fonctionnalité|
|DIAGRAMNET-50541 | VSDX en conversion PDF, les éléments de texte en hébreu sont rendus dans l'ordre inverse.| Renforcement|
|DIAGRAMNET-50542 | VSD en conversion PDF, le mot arabe se transforme en lettres.| Renforcement|
|DIAGRAMNET-50682 | VSD à l'export PDF, le texte de la cellule du tableau est partiellement invisible.| Punaise|
|DIAGRAMNET-50712 | VDX vers exportation PDF - le texte de différentes formes est mal placé.| Punaise|
|DIAGRAMNET-50741 | VSD à l'exportation SVG manque certaines formes Visio.| Punaise|
|DIAGRAMNET-50742 | VSD à l'exportation SVG n'applique pas la couleur blanche intérieure des formes.| Punaise|
|DIAGRAMNET-50744 |La routine d'ouverture et de sauvegarde de VSDX a changé le texte en caractères factices.| Punaise|
|DIAGRAMNET-50745 | La routine d'ouverture et de sauvegarde de VSDX a modifié le modeleur de ligne pointillée.| Punaise|
|DIAGRAMNET-50748 | VSD vers l'exportation PDF - les éléments de texte sont mal placés.| Punaise|
|DIAGRAMNET-50763 | L'exportation VSD à VDX génère l'erreur d'élément maître.| Punaise|
### **Public API et modifications incompatibles avec les versions antérieures**
Consultez la liste des modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée au Aspose.Diagram for .NET. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
#### **Ajouter les classes FileFormatUtil et FileFormatInfo**
Ces classes donnent un accès par programme pour détecter le type de fichier Visio.
#### **Ajoute la méthode DetectFileFormat dans la classe FileFormatUtil**
Il détecte et renvoie les informations sur le format d'un Visio diagram stocké dans un fichier.
#### **Ajoute la propriété FileFormatType dans la classe FileFormatInfo**
Il obtient le format de fichier détecté.
#### **Ajoute la propriété LoadFormat dans FileFormatInfo**
Il obtient le format de chargement détecté.
#### **Ajoute la propriété ExportHiddenPage dans les classes SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions et PdfSaveOptions**
Il définit s'il faut exporter les pages Visio masquées ou non.
### **Exemples d'utilisation**
Veuillez consulter la liste des rubriques d'aide ajoutées dans les documents Wiki Aspose.Diagram :

- [Contrôler l'exportation des pages masquées Visio lors de l'enregistrement](/diagram/fr/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
- [Détecter le format du fichier Visio](/diagram/fr/net/introduction/#detect-the-format-of-visio-file)
