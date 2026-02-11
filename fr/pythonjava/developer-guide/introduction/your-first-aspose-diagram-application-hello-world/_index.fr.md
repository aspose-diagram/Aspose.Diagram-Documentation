---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /fr/python-java/your-first-aspose-diagram-application-hello-world/
description: Cette page décrit comment créer la première application avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. Créez une instance de la classe Diagram.
1. Appliquer la licence :
 1. Si vous avez acheté une licence, utilisez la licence dans votre application pour accéder à toutes les fonctionnalités de Aspose.Diagram.
 1. Si vous utilisez la version d'évaluation du composant (si vous utilisez Aspose.Diagram sans licence), ignorez cette étape.
1. Créez un nouveau fichier Visio ou ouvrez un fichier Visio existant.
1. Créez une nouvelle zone de texte.
1.  Insérez les mots**Hello World!** dans une zone de texte.
1. Générez le fichier Microsoft Visio modifié.

La mise en œuvre des étapes ci-dessus est illustrée dans les exemples ci-dessous.

### **Code Sample: Creating a New Diagram and Writing Hello World!**

L'exemple suivant ouvre un fichier de modèle Microsoft Visio existant nommé "[Basic_Shapes.vss](Basic_Shapes.vss)", inputs "Hello World!" text in the first page and saves the diagram.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Basic_Shapes.vss")

# Add a new hello world rectangle shape
shapeId = diagram.addShape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.getPages().getPage(0).getShapes().getShape(shapeId)
shape.getText().getValue().add(Txt("Hello World"))

# Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
