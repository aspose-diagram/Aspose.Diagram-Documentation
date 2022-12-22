---
title: Utilisation de Aspose.Diagram dans d'autres langages de programmation
type: docs
weight: 120
url: /fr/net/utilizing-aspose-diagram-in-other-programming-languages/
description: Cette page décrit comment utiliser Aspose.Diagram dans d'autres langages de programmation.
---
## **Use Aspose.Diagram for .NET via COM Interop**
 Les informations de cette rubrique s'appliquent aux scénarios dans lesquels les développeurs doivent utiliser[Aspose.Diagram for .NET](/diagram/fr/net/home/) via COM Interop in any supported language.
### **Travailler avec COM Interop**
Aspose.Diagram for .NET executes under the control of the .NET Framework and this is called managed code. The code written in all of the languages those runs outside the .NET Framework and it is called unmanaged code. Interaction between unmanaged code and Aspose.Diagram occurs via the .NET facility called COM Interop.

Aspose.Diagram objects are .NET objects, but when used via COM Interop, they appear as COM objects in your programming language. Therefore, it is best to make sure you know how to create and use COM objects in your programming language, before you start using [Aspose.Diagram for .NET](/diagram/fr/net/home/).

- Dans le monde COM, nous distinguons le serveur COM et le client COM. Le serveur COM a stocké les classes COM tandis que le client COM demande au serveur COM des instances de classes, c'est-à-dire des objets COM.
-  Le client COM ou simplement l'application cliente peut connaître quelque chose sur le contenu de la classe COM ou ignorer totalement ses méthodes et ses propriétés. Par conséquent, l'application cliente peut découvrir la structure de la classe COM lors de la compilation/construction ou uniquement lors de l'exécution. Le processus de "découverte" est connu sous le nom de liaison et nous avons donc**reliure précoce** et**reliure tardive**.
- en bref, la classe COM est comme une boîte noire et pour travailler avec elle, une bibliothèque de types est nécessaire, ce fichier binaire contient une description des méthodes de classe COM, des propriétés et de tout langage de haut niveau qui prend en charge le travail avec des objets COM a souvent une expression de syntaxe pour ajouter une bibliothèque de types, pour par exemple c'est[**#importer**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) au C++.
- la bibliothèque de types est utilisée pour la liaison anticipée.
-  un objet COM peut exposer ses méthodes et propriétés de deux manières : au moyen d'un**interface de répartition** (dispinterface) et dans son**vtable** (table de fonction virtuelle).
-  au sein de la**interface d'affichage** , chaque méthode et propriété est identifiée par un membre unique ; ce membre est l'identifiant de répartition de la fonction (ou**DispID**).
- **vtable** est juste un ensemble de pointeurs vers des fonctions prises en charge par l'interface de classe COM.
-  un objet qui expose ses méthodes via les deux interfaces prend en charge un**double interface**.
- les deux types de reliure présentent des avantages. La liaison anticipée vous offre des performances accrues et une vérification de la syntaxe au moment de la compilation. La reliure tardive est plus avantageuse lorsque vous écrivez des clients que vous avez l'intention d'être***compatible avec les futures versions*** de votre classe COM. Avec la liaison tardive, les informations de la bibliothèque de types ne sont pas "câblées" dans votre client, vous pouvez donc avoir une plus grande confiance dans le fait que votre client peut travailler avec les futures versions de la classe COM sans modifications de code.
-  le mécanisme de liaison tardive présente un gros avantage : si le créateur de la DLL COM décide de publier une nouvelle version, avec une disposition d'interface de fonction différente, tout code appelant ces méthodes ne plantera pas à moins que les méthodes ne soient plus disponibles ; même si le**vtable**Cette liaison tardive différente parvient à découvrir les nouveaux DISPID et à appeler les méthodes appropriées.

 Voici les sujets que vous devrez éventuellement maîtriser :

- Utiliser des objets COM dans votre langage de programmation. Consultez la documentation de votre langage de programmation et les rubriques spécifiques au langage plus loin dans cette documentation.
-  Travailler avec des objets COM exposés par .NET COM Interop. Voir[Interopérer avec du code non managé](https://docs.microsoft.com/en-us/dotnet/framework/interop/) et[Exposition des composants .NET Framework à COM](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com) dans MSDN.
-  Aspose.Diagram modèle d'objet de document. Voir[Aspose.Diagram Guide du programmeur](https://docs.aspose.com/diagram/net/developer-guide/) et[API Référence](https://reference.aspose.com/diagram/net).
#### **Enregistrez Aspose.Diagram for .NET avec COM Interop**
Vous devez installer Aspose.Diagram for .NET et vous assurer qu'il est enregistré auprès de COM Interop (en veillant à ce qu'il puisse être appelé à partir de code non géré).

Pour enregistrer manuellement Aspose.Diagram for .NET pour COM Interop :

1.  Du**Commencer** menu, sélectionnez**Tous les programmes** , alors**Microsoft Visual Studio**, **Visual Studio Tools** et enfin,**Visual Studio Command Prompt**. Dans certains systèmes d'exploitation, il est également disponible à l'emplacement : "C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64"
1.  Saisissez la commande pour enregistrer l'assembly :
   1. .NET Framework 2.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /codebase
   1. .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /codebase
   1. .NET Framework 4.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /codebase

{{% alert color="primary" %}} 

Faites attention que /codebase n'est nécessaire que si Aspose.Diagram.dll n'est pas dans GAC, l'utilisation de cette option oblige regasm à mettre le chemin pour l'assemblage dans le registre.

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe est un outil inclus dans .NET Framework SDK. Tous les outils SDK .NET Framework sont situés dans le*\Microsoft .NET\Framevork\<FrameworkVersion>* répertoire, par exemple*C:\Windows\Microsoft .NET\Framework\v4.0.30319*. If you use Visual Studio .NET:
 Du**Commencer** menu, sélectionnez**Programmes** , suivie par**Microsoft Visual Studio .NET** , alors**Visual Studio .NET Tools** et enfin,**Visual Studio .NET 2003 Command Prompt**.
Il exécute une invite de commande avec toutes les variables d'environnement nécessaires définies.

{{% /alert %}} 
##### **ProgID**
ProgID signifie "identifiant programmatique". C'est le nom d'une classe COM utilisée pour créer un objet. Les ProgID se composent du nom de la bibliothèque "Aspose.Diagram" et du nom de la classe.
##### **Bibliothèque de types**
Si votre langage de programmation (par exemple Visual Basic ou Delphi) vous permet de référencer une bibliothèque de types COM, ajoutez une référence à Aspose.Diagram.tlb et pour voir toutes les classes, méthodes, propriétés et énumérations Aspose.Diagram for .NET dans votre Explorateur d'objets.

Pour générer un fichier TLB :

- .NET Framework 2.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.tlb" /codebase
- .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.tlb" /codebase
- .NET Framework 4.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.tlb" /codebase
#### **Création d'objets COM**
La création d'un objet COM est similaire à la création d'un objet .NET normal. Une fois créé, vous pouvez accéder aux méthodes et propriétés de l'objet, comme s'il s'agissait d'un objet COM.

Certaines méthodes ont des surcharges et elles seront exposées par COM Interop avec un suffixe numérique ajouté, à l'exception de la toute première méthode qui reste inchangée. Par exemple, les surcharges de la méthode Diagram.Save deviennent Diagram.Save, Diagram.Save_2, etc.

{{% alert color="primary" %}} 

 Pour plus d'informations, consultez les articles spécifiques à la langue plus loin dans cette documentation.

{{% /alert %}} 
## **Aspose.Diagram Ressources**
Vous trouverez ci-dessous des liens vers des ressources utiles dont vous pourriez avoir besoin pour accomplir vos tâches.
- [Aspose.Diagram for Java Documentation en ligne](https://docs.aspose.com/diagram/java/)
- [Aspose.Diagram for Node.js via Java Online Documentation](https://docs.aspose.com/diagram/nodejsjava/)
- [Aspose.Diagram for Python via Java Online Documentation](https://docs.aspose.com/diagram/pythonjava/)

##### **Création d'un assemblage wrapper**
Si vous devez utiliser de nombreuses classes, méthodes et propriétés Aspose.Diagram for .NET, envisagez de créer un assembly wrapper (en utilisant C# ou tout autre langage de programmation .NET). Les assemblys wrapper permettent d'éviter d'utiliser Aspose.Diagram for .NET directement à partir de code non managé.

Une bonne approche consiste à développer un assembly .NET qui référence Aspose.Diagram for .NET et fait tout le travail avec, et n'expose qu'un ensemble minimal de classes et de méthodes au code non managé. Votre application devrait alors fonctionner uniquement avec votre bibliothèque wrapper.

Reducing the number of classes and methods that you need to invoke via COM Interop simplifies the project. Using .NET classes via COM Interop often requires advanced skills. 
## **Créer un dessin vide Visio en PHP à l'aide de COM Interop**
### **Conditions préalables**
 Configurez votre PHP pour qu'il fonctionne avec COM. Voir<http://www.php.net/manual/en/ref.com.php> . Pour plus d'informations, veuillez consulter l'article intitulé[Use Aspose.Diagram for .NET via COM Interop](/diagram/fr/net/home/).
### **Création d'un dessin Visio vide**
 Ceci est une application simple qui vous montre comment créer un dessin vide Visio en utilisant[Aspose.Diagram for .NET](/diagram/fr/net/home/) in PHP via COM Interop.

**PHP**

{{< highlight "csharp" >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
