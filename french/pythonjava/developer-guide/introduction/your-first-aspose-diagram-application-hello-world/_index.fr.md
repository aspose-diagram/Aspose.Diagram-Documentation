---
title: Votre première application Aspose.Diagram - Hello World
type: docs
weight: 30
url: /fr/python-java/your-first-aspose-diagram-application-hello-world/
description: Cette page décrit comment créer la première application avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

Ce tutoriel montre comment créer une toute première application (Hello World) en utilisant Aspose.Diagram' simple API. Cette application simple crée un fichier Microsoft Visio avec le texte 'Hello World' dans une Page spécifiée.

{{% /alert %}}

## **Création de l'application Hello World**

Les étapes ci-dessous créent l'application Hello World à l'aide du Aspose.Diagram API :

1. Créez une instance de la classe Diagram.
1. Appliquer la licence :
 1. Si vous avez acheté une licence, utilisez la licence dans votre application pour accéder à toutes les fonctionnalités de Aspose.Diagram.
 1. Si vous utilisez la version d'évaluation du composant (si vous utilisez Aspose.Diagram sans licence), ignorez cette étape.
1. Créez un nouveau fichier Visio ou ouvrez un fichier Visio existant.
1. Créez une nouvelle zone de texte.
1.  Insérez les mots**Bonjour le monde!** dans une zone de texte.
1. Générez le fichier Microsoft Visio modifié.

La mise en œuvre des étapes ci-dessus est illustrée dans les exemples ci-dessous.

### **Exemple de code : Création d'un nouveau Diagram et écriture de Hello World !**

L'exemple suivant ouvre un fichier de modèle Microsoft Visio existant nommé "[Basic_Shapes.vss](Basic_Shapes.vss)", saisit le texte "Hello World!" dans la première page et enregistre le diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-CreatingHelloWorldVisioFile.py" >}}
