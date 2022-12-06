---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /fr/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

This beginner's topic shows how developers can create a simple first application (Hello World) using Aspose.Diagram' simple API. The application creates a Microsoft Visio file with the words Hello World in the page.

{{% /alert %}}

### **Creating the Hello World Application**

To create the Hello World application using Aspose.Diagram API:

1. Créez une instance de la classe Workbook.
1. Appliquer la licence :
 1. Si vous avez acheté une licence, utilisez la licence dans votre application pour accéder à toutes les fonctionnalités de Aspose.Diagram.
 1. Si vous utilisez la version d'évaluation du composant (si vous utilisez Aspose.Diagram sans licence), ignorez cette étape.
1. Créez un nouveau fichier Microsoft Visio ou ouvrez un fichier existant dans lequel vous souhaitez ajouter/mettre à jour du texte.
1.  Insérez les mots**Hello World!** dans la page consultée.
1. Générez le fichier Microsoft Visio modifié.

Les exemples ci-dessous illustrent les étapes ci-dessus.

#### **Création d'un Diagram**

The following example creates a new diagram from scratch, writes the words "Hello World!" on the first page, and saves the file.

**Créer un nouveau fichier visio** 

![tâche : image_autre_texte](your-first-aspose-diagram-application-hello-world_1.png)

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **Ouvrir un fichier existant**

The following example opens an existing Microsoft Visio template file, writes the words "Hello World!" in the first page, and saves the diagram as a new file.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
