---
title: Utilisation du paragraphe Formes
type: docs
weight: 40
url: /fr/java/working-with-shapes-paragraph/
---
Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. Accéder à une forme particulière.
1. Définissez le paragraphe de la forme.
#### **Définir l'exemple de programmation de paragraphe de la forme**
Utilisez le code suivant dans votre application Java pour définir le paragraphe de la forme à l'aide de Aspose.Diagram for Java.

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