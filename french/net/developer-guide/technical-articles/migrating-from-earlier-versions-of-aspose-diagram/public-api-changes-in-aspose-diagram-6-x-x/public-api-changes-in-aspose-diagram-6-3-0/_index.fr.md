---
title: Public API Changements dans Aspose.Diagram 6.3.0
type: docs
weight: 30
url: /fr/net/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 6.0.0 à 6.3.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **Détecter le format d'un fichier Visio**
**Diverses classes, méthodes et propriétés sont ajoutées pour détecter le format**
- **Ajouter les classes FileFormatUtil et FileFormatInfo** 
 - Ces classes donnent un accès programmatique pour détecter le type de fichier Visio.
- **Ajoute la méthode DetectFileFormat dans la classe FileFormatUtil** 
 - Il détecte et renvoie les informations sur le format d'un Visio diagram stocké dans un fichier.
- **Ajoute la propriété FileFormatType dans la classe FileFormatInfo** 
 - Il obtient le format de fichier détecté.
- **Ajoute la propriété LoadFormat dans FileFormatInfo** 
 - Il obtient le format de chargement détecté.

 Les développeurs peuvent facilement détecter le format de n'importe quel fichier Visio. Cette rubrique d'aide explique comment détecter le format de fichier Visio (à l'aide d'un chemin de fichier ou d'un flux) et vérifier son extension :[Détecter le format du fichier Visio](/diagram/fr/net/introduction/#detect-the-format-of-visio-file)
## **Contrôler l'exportation des pages masquées Visio lors de l'enregistrement**
**Ajoute la propriété ExportHiddenPage dans les classes SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions et PdfSaveOptions**
- Il définit s'il faut exporter les pages Visio masquées ou non.

 Les développeurs peuvent inclure ou exclure des pages Visio masquées lors de l'enregistrement d'un Visio diagram dans des fichiers PDF, HTML, image (PNG, JPEG, GIF), SVG et XPS. Cette rubrique d'aide illustre comment procéder :[Contrôler l'exportation des pages masquées Visio lors de l'enregistrement](/diagram/fr/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
