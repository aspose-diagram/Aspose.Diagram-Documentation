---
title: Vérifiez si le code VBA est signé
type: docs
weight: 100
url: /fr/net/check-if-vba-code-is-signed/
description: Vérifiez si le code vba est signé avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram permet à l'utilisateur de vérifier si le projet de code VBA est signé ou non. Veuillez utiliser le[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) propriété pour vérifier si le projet de code VBA est signé ou non.

{{% /alert %}}

 Le code suivant explique comment vérifier si le code VBA est signé ou non en utilisant le[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) propriété. Vous pouvez utiliser n'importe lequel de vos fichiers visio pour tester ce code. À des fins de test, vous pouvez utiliser[ce fichier visio utilisé dans le code](1.vsdm).

## Exemple de code

```
{{< highlight "csharp" >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Sortie console

 Vous trouverez ci-dessous la sortie de la console du code ci-dessus en utilisant le[exemple de fichier visio](1out.vsdm) fourni par le lien.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
