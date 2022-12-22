---
title: Gérer les codes VBA de Visio Macro-Enabled diagram.
linktitle: Diagram Projet VBA
type: docs
weight: 200
url: /fr/net/working-with-vbaproject/
description: Ajoutez un module VBA et modifiez VBA ou une macro avec la bibliothèque Aspose.Diagram.
---
## **Ajouter un module VBA**
{{% alert color="primary" %}}

 Aspose.Diagram vous permet d'ajouter un nouveau module VBA et un code macro à l'aide de Aspose.Diagram. Veuillez utiliser le[**Diagram.VbaProject.Modules.Add()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) méthode pour ajouter le nouveau module VBA à l'intérieur du diagram

{{% /alert %}}

 L'exemple de code suivant ajoute un nouveau module VBA et un code macro et enregistre la sortie au format VSDM. Une fois, vous ouvrirez le fichier de sortie VSDM dans Microsoft Visio et cliquez sur le**Développeur > Visual Basic** commandes de menu, vous verrez un module nommé "TestModule" et à l'intérieur, vous verrez le code macro suivant.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Voici l'exemple de code pour générer le fichier de sortie VSDM avec le module VBA et le code macro.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-AddModule.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-ModifyModule.cs" >}}

## **Sujets avancés**
- [Vérifiez si le code VBA est signé](/diagram/fr/net/check-if-vba-code-is-signed/)
