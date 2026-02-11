---
title: Licence
type: docs
weight: 50
url: /fr/net/licensing/
description: Aspose. Diagram for .NET invite ses clients à obtenir une licence classique et une licence mesurée. En plus d'utiliser une licence limitée pour mieux explorer le produit.
---
## **Évaluer Aspose.Diagram**
Vous pouvez facilement télécharger le produit Aspose.Diagram for .NET à des fins d'évaluation. Veuillez vous référer au[Aspose.Diagram for .NET page de téléchargement](https://www.nuget.org/packages/Aspose.Diagram/)pour connaître la dernière version. Le téléchargement d'évaluation est identique au téléchargement acheté. La version d'évaluation devient simplement sous licence lorsque vous ajoutez quelques lignes de code pour appliquer la licence.

La version d'évaluation de Aspose.Diagram (sans licence spécifiée) fournit toutes les fonctionnalités du produit, mais elle insère un filigrane d'évaluation au milieu du document lors de l'ouverture et de l'enregistrement, et limite la lecture des dix premières formes de la première page de votre Visio diagram .

![tâche : image_autre_texte](licensing_1.png)
### **Limites de la version d'évaluation**
La version d'évaluation fournit toutes les fonctionnalités à l'exception des suivantes :

- Vous ne pouvez lire que les dix premières formes de la première page de Visio diagram.
- You will also see evaluation watermark in exported images and PDF files.

{{% alert color="primary" %}} 

 Si vous souhaitez essayer Aspose.Diagram sans limitations d'évaluation, demandez une licence temporaire de 30 jours. Prière de se référer à[Comment obtenir une licence temporaire ?](https://purchase.aspose.com/temporary-license) pour plus d'informations.

{{% /alert %}} 
## **Appliquer une licence**
Une fois que vous êtes satisfait de votre[évaluation](https://downloads.aspose.com/diagram/net) du Aspose.Diagram for .NET, achetez une licence sur le site Aspose :[Portail d'achat](https://purchase.aspose.com/buy) . Familiarisez-vous avec les différents types de licences disponibles. Si vous avez des questions,[contacter l'équipe commerciale Aspose](https://about.aspose.com/contact) et ils seront heureux de vous aider.

Chaque licence Aspose comporte un abonnement d'un an pour des mises à niveau gratuites vers toutes les nouvelles versions ou correctifs qui sortent pendant cette période. Nous fournissons un support technique gratuit et illimité aux utilisateurs sous licence et d'évaluation.

La licence est un fichier XML en texte brut qui contient des détails tels que le nom du produit, le nombre de développeurs sous licence, la date d'expiration de l'abonnement, etc. Le fichier est signé numériquement, ne modifiez donc pas le fichier : même l'ajout d'un saut de ligne supplémentaire au fichier l'invalide.
### **Quand appliquer une licence**
Suivez ces règles simples :

- La licence ne doit être définie qu'une seule fois par domaine d'application.
- Vous devez définir la licence avant d'utiliser toute autre classe Aspose.Diagram.
- Appeler SetLicense plusieurs fois n'est pas dangereux, mais fait perdre du temps au processeur.
- Si vous développez une application Windows Forms ou console, appelez SetLicense dans le code de démarrage avant d'utiliser les classes Aspose.Diagram.
- Lors du développement d'une application ASP.NET, appelez SetLicense à partir du fichier Global.asax.cs, dans la méthode protégée Aplication_Start. Il est appelé une fois au démarrage de l'application.
- N'appelez pas SetLicense à partir des méthodes Page_Load car cela signifie que la licence sera chargée à chaque chargement d'une page Web.
- Si vous développez une bibliothèque de classes, vous appelez SetLicense à partir d'un constructeur statique de la classe qui utilise Aspose.Diagram. Le constructeur statique s'exécute avant qu'une instance de votre classe soit créée en s'assurant que la licence Aspose.Diagram est correctement définie.
### **Appliquer la licence à l'aide d'un fichier ou d'un objet de flux**
 Utilisez le[Licence.SetLicense](https://reference.aspose.com/diagram/net/aspose.diagram/license)méthode pour obtenir la licence du composant. Le moyen le plus simple de définir une licence consiste à placer le fichier de licence dans le même dossier que Aspose.Diagram.dll et à spécifier le nom du fichier, sans chemin, comme indiqué ci-dessous.
#### **Chargement d'une licence à partir d'un fichier**
Cet extrait de code initialise une licence stockée dans un fichier ou dans une ressource intégrée.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";

License license = new License();
license.SetLicense(dataDir + "Aspose.Diagram.lic");

{{< /highlight >}}

#### **Chargement d'une licence à partir d'un objet de flux**
Ces extraits de code initialisent la licence à partir du flux.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";
// Load an existing Visio file in the stream
FileStream LicStream = new FileStream(dataDir + "Aspose.Diagram.lic", FileMode.Open);

License license = new License();
license.SetLicense(LicStream);

{{< /highlight >}}

## **Appliquer une licence limitée**
Aspose.Diagram for .NET API permet aux développeurs d'appliquer une licence limitée. Il s'agit d'un nouveau mécanisme d'octroi de licences. Le nouveau mécanisme d'octroi de licences sera utilisé avec la méthode d'octroi de licences existante. Les clients qui souhaitent être facturés en fonction de l'utilisation des fonctionnalités API peuvent utiliser la licence mesurée. Pour plus de détails, veuillez consulter[FAQ sur les licences limitées](https://purchase.aspose.com/faqs/licensing/metered)section.

Une nouvelle classe[Compteur](https://reference.aspose.com/diagram/net/aspose.diagram/metered)a été ajouté pour appliquer la clé mesurée. Cet exemple de code montre comment définir des clés publiques et privées limitées :


{{< highlight csharp >}}
// Initialize a Metered license class object
Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();
// apply public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}

