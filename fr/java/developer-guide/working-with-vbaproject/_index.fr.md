---
title: Gérer les codes VBA de Visio Macro-Enabled diagram.
linktitle: Diagram Projet VBA
type: docs
weight: 200
url: /fr/java/working-with-vbaproject/
description: Ajoutez un module VBA et modifiez VBA ou une macro avec la bibliothèque Aspose.Diagram.
---
## **Ajouter un module VBA**
{{% alert color="primary" %}}

Aspose.Diagram vous permet d'ajouter un nouveau module VBA et un code macro à l'aide de Aspose.Diagram. Veuillez utiliser la méthode [**Diagram.VbaProject.Modules.Add()**] pour ajouter le nouveau module VBA dans le diagram

{{% /alert %}}

 L'exemple de code suivant ajoute un nouveau module VBA et un code macro et enregistre la sortie au format VSDM. Une fois, vous ouvrirez le fichier de sortie VSDM dans Microsoft Visio et cliquez sur le**Développeur > Visual Basic** commandes de menu, vous verrez un module nommé "TestModule" et à l'intérieur, vous verrez le code macro suivant.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Voici l'exemple de code pour générer le fichier de sortie VSDM avec le module VBA et le code macro.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.getVbaProject().getModules().add(VbaModuleType.PROCEDURAL, "TestModule");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(index);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Modifier VBA ou Macro**

{{% alert color="primary" %}} 

Vous pouvez modifier VBA ou Macro Code à l'aide de Aspose.Diagram. Aspose.Diagram a ajouté l'espace de noms et les classes suivants pour lire et modifier le projet VBA dans le fichier Visio.

- Aspose.Diagram.Vba
- Projet Vba
- VbaModuleCollectionVbaModuleCollection
- Module Vba

Cet article vous montrera comment modifier le code VBA ou macro dans le fichier source Visio à l'aide de Aspose.Diagram.

{{% /alert %}} 

L'exemple de code suivant charge le fichier source Visio qui contient un code VBA ou Macro suivant à l'intérieur

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

Après l'exécution de l'exemple de code Aspose.Diagram, le code VBA ou Macro sera modifié comme ceci

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 Vous pouvez télécharger le[fichier source Visio]() et le[fichier de sortie Visio]() à partir des liens donnés.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(2);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Sujets avancés**
- [Vérifiez si le code VBA est signé](/diagram/fr/java/check-if-vba-code-is-signed/)
