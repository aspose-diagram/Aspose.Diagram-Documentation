---
title: Votre première application Aspose.Diagram - Hello World
type: docs
weight: 30
url: /fr/java/your-first-aspose-diagram-application-hello-world/
description: Cette page décrit comment créer la première application avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

Ce tutoriel montre comment créer une toute première application (Hello World) en utilisant Aspose.Diagram' simple API. Cette application simple crée un fichier Microsoft Visio avec le texte 'Hello World' dans une Page spécifiée.

{{% /alert %}}

## **Création de l'application Hello World**

Les étapes ci-dessous créent l'application Hello World à l'aide du Aspose.Diagram API :

1.  Créer une instance de[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classer.
1.  Si vous avez une licence, alors[appliquez-le](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 Si vous utilisez la version d'évaluation, ignorez les lignes de code liées à la licence.
1. Créez un nouveau fichier Visio ou ouvrez un fichier Visio existant.
1. Créez une nouvelle zone de texte.
1.  Insérez les mots**Bonjour le monde!** dans une zone de texte.
1. Générez le fichier Microsoft Visio modifié.

La mise en œuvre des étapes ci-dessus est illustrée dans les exemples ci-dessous.

### **Exemple de code : création d'un nouveau Diagram**

L'exemple suivant crée un nouveau diagram à partir de zéro, écrit Hello World! sur la première page et enregistre le fichier Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **Exemple de code : ouverture d'un fichier existant**

L'exemple suivant ouvre un fichier de modèle Microsoft Visio existant nommé "Sample.vsdx", entre "Hello World!" texte dans la première page et enregistre le diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
