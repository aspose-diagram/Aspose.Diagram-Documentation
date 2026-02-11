---
title: Vérifiez si le code VBA est signé
type: docs
weight: 100
url: /fr/java/check-if-vba-code-is-signed/
description: Vérifiez si le code vba est signé avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram permet à l'utilisateur de vérifier si le projet de code VBA est signé ou non. Veuillez utiliser la propriété [**Diagram.VbaProject.IsSigned**] pour vérifier si le projet de code VBA est signé ou non.

{{% /alert %}}

 Le code suivant explique comment vérifier si le code VBA est signé ou non à l'aide de la propriété [**Diagram.VbaProject.IsSigned**]. Vous pouvez utiliser n'importe lequel de vos fichiers visio pour tester ce code. À des fins de test, vous pouvez utiliser[ce fichier visio utilisé dans le code](1.vsdm).

## Exemple de code

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Sortie console

 Vous trouverez ci-dessous la sortie de la console du code ci-dessus en utilisant le[exemple de fichier visio](1out.vsdm) fourni par le lien.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
