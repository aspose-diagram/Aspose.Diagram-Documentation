---
title: Différentes façons d'ouvrir des fichiers
type: docs
weight: 10
url: /fr/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Avec Aspose.Diagram, il est simple d'ouvrir des fichiers, par exemple pour récupérer des données, ou d'utiliser un modèle de concepteur pour accélérer le processus de développement.

{{% /alert %}}

## **Opening a File via a Path**

 Les développeurs peuvent ouvrir un fichier Microsoft Diagram en utilisant son chemin de fichier sur l'ordinateur local en le spécifiant dans le**Diagram**constructeur de classe. Passez simplement le chemin dans le constructeur en tant que*chaîne de caractères*. Aspose.Diagram détectera automatiquement le type de format de fichier.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **Opening a File via a Stream**

 Il est également simple d'ouvrir un fichier Visio en tant que flux. Pour ce faire, utilisez une version surchargée du constructeur qui prend le*BufferStream*objet qui contient le fichier.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **Ouvrir un fichier avec LoadOptions**

 Pour ouvrir un fichier avec loadoptions, utilisez le**ChargerOptions**classes pour définir les options associées des classes pour le fichier modèle à charger.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

