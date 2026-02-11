---
title: Licence
type: docs
weight: 60
url: /fr/java/licensing/
---
## **Limites de la version d'évaluation**
 Une version d'évaluation gratuite de Aspose.Diagram for Java peut être téléchargée à partir de[Aspose Référentiel](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **Limitation**
La version d'évaluation fournit toutes les fonctionnalités à l'exception des suivantes :

- Vous ne pouvez lire que les dix premières formes de la première page de votre fichier VSD.
- You will also see evaluation watermark in exoprted images and PDF files.

 Si vous souhaitez essayer Aspose.Diagram sans limitations d'évaluation, demandez une licence temporaire de 30 jours. Prière de se référer à[Comment obtenir une licence temporaire ?](https://purchase.aspose.com/temporary-license) pour plus d'informations.
## **Appliquer une licence**
 Vous pouvez télécharger une version d'évaluation de**Aspose.Diagram** for Java de[Aspose Référentiel](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). La version d'évaluation fournit absolument les mêmes fonctionnalités que la version sous licence du produit. De plus, la version d'évaluation devient simplement sous licence lorsque vous achetez une licence et ajoutez quelques lignes de code pour appliquer la licence.

 Une fois que vous êtes satisfait de votre évaluation de**Aspose.Diagram** , tu peux[acheter une licence](https://purchase.aspose.com/buy) sur le site Aspose. Familiarisez-vous avec les différents types d'abonnements proposés. Si vous avez des questions, n'hésitez pas à contacter l'équipe commerciale au Aspose.

Chaque licence Aspose comporte un abonnement d'un an pour des mises à niveau gratuites vers toutes les nouvelles versions ou correctifs qui sortent pendant cette période. Le support technique est gratuit et illimité et fourni à la fois aux utilisateurs sous licence et aux utilisateurs d'évaluation.

{{% alert color="primary" %}} 

 Si vous voulez tester**Aspose.Diagram** sans limitation de version d'évaluation, demandez une licence temporaire de 30 jours. Prière de se référer à[Comment obtenir une licence temporaire ?](https://purchase.aspose.com/temporary-license) pour plus d'informations.

{{% /alert %}} 
### **Définition d'une licence**
La licence est un fichier XML en texte brut qui contient des détails tels que le nom du produit, le nombre de développeurs auxquels il est licencié, la date d'expiration de l'abonnement, etc. Le fichier est signé numériquement, ne modifiez donc pas le fichier ; même l'ajout par inadvertance d'un saut de ligne supplémentaire dans le fichier l'invalidera.

Vous devez appliquer une licence avant d'effectuer toute opération avec des documents. Assurez-vous de le faire avant de créer un objet Diagram. Vous n'êtes tenu de définir une licence qu'une seule fois par application ou processus.

La licence peut être chargée à partir d'un flux ou d'un fichier aux emplacements suivants :

1. Chemin explicite.
1. Le dossier qui contient le fichier Aspose.Diagram.jar.

 Utilisez le[Licence.setLicense()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License) méthode pour obtenir la licence du composant. Souvent, le moyen le plus simple de définir une licence consiste à placer le fichier de licence dans le même dossier que Aspose.Diagram.jar et à spécifier uniquement le nom du fichier sans chemin, comme indiqué dans l'exemple suivant :
#### **Exemple 1**
 Dans cet exemple**Aspose.Diagram** tentera de trouver le fichier de licence dans le dossier contenant les fichiers JAR de votre application.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **Exemple 2**
Initialise une licence à partir d'un flux.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **Valider la licence**
 Il est possible de valider si la licence a été configurée correctement ou non. La[Licence](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)class a le champ isLicensed qui renverra true si la licence a été correctement définie.

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Appliquer une licence limitée**
Aspose.Diagram for Java API permet aux développeurs d'appliquer une licence limitée. Il s'agit d'un nouveau mécanisme d'octroi de licences. Le nouveau mécanisme d'octroi de licences sera utilisé avec la méthode d'octroi de licences existante. Les clients qui souhaitent être facturés en fonction de l'utilisation des fonctionnalités API peuvent utiliser la licence mesurée. Pour plus de détails, veuillez consulter[FAQ sur les licences limitées](https://purchase.aspose.com/faqs/licensing/metered)section.

Une nouvelle classe[Compteur](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered) a été ajouté pour appliquer la clé mesurée. Cet exemple de code montre comment définir des clés publiques et privées limitées :

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// Initialize a Metered license class object
Metered metered = new Metered();
// apply public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```
