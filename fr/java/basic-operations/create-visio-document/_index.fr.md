---
title: Créer le document Visio par programme
linktitle: Créer un document Visio
type: docs
weight: 10
url: /fr/java/create-visio-document/
description: Cette page décrit comment créer un document Visio à partir de zéro avec la bibliothèque Aspose.Diagram.
---
## **Création d'un nouveau dessin Visio**
Aspose.Diagram for Java vous permet de lire et de créer des diagrammes Microsoft Visio à partir de vos propres applications, sans Microsoft Office Automation. La première étape lors de la création de nouveaux documents consiste à créer un diagram. Ajoutez ensuite des formes et des connecteurs pour créer le diagram.
### **Créer un exemple de programmation de dessin Visio**
Le code ci-dessous montre comment créer un nouveau dessin Microsoft Visio. Veuillez noter que le dessin vierge contient une seule page vide.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

{{% alert color="primary" %}} 

Le format de papier à dessin est Lettre par défaut.

{{% /alert %}} 

