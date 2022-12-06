---
title: Votre première application Aspose.Diagram - Hello World
type: docs
weight: 30
url: /fr/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

Cette rubrique pour débutant montre comment les développeurs peuvent créer une première application simple (Hello World) en utilisant Aspose.Diagram' simple API. L'application crée un fichier Microsoft Visio avec les mots Hello World dans la page.

{{% /alert %}}

### **Création de l'application Hello World**

Pour créer l'application Hello World en utilisant Aspose.Diagram API :

1. Créez une instance de la classe Workbook.
1. Appliquer la licence :
 1. Si vous avez acheté une licence, utilisez la licence dans votre application pour accéder à toutes les fonctionnalités de Aspose.Diagram.
 1. Si vous utilisez la version d'évaluation du composant (si vous utilisez Aspose.Diagram sans licence), ignorez cette étape.
1. Créez un nouveau fichier Microsoft Visio ou ouvrez un fichier existant dans lequel vous souhaitez ajouter/mettre à jour du texte.
1.  Insérez les mots**Bonjour le monde!** dans la page consultée.
1. Générez le fichier Microsoft Visio modifié.

Les exemples ci-dessous illustrent les étapes ci-dessus.

#### **Création d'un Diagram**

L'exemple suivant crée un nouveau diagram à partir de zéro, écrit les mots "Hello World!" sur la première page et enregistre le fichier.

**Créer un nouveau fichier visio** 

![tâche : image_autre_texte](your-first-aspose-diagram-application-hello-world_1.png)

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **Ouvrir un fichier existant**

L'exemple suivant ouvre un fichier de modèle Microsoft Visio existant, écrit les mots "Hello World!" dans la première page, et enregistre le diagram en tant que nouveau fichier.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
