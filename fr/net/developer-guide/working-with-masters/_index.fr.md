---
title: Travailler avec les maîtres
type: docs
weight: 70
url: /fr/net/working-with-masters/
description: Cette section explique comment ajouter un maître ou obtenir des informations sur le maître avec Aspose.Diagram.
---
## **Récupération des informations sur le maître**
Un maître de forme est un autre nom pour un gabarit Visio. Avec Aspose.Diagram, il est possible de récupérer des informations sur les pages, les connecteurs et aussi les masters. Cet article explique comment obtenir l'ID et le nom d'un diagram.

 La[Maître](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'objet représente un[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maître de l'objet dans un diagram. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour récupérer les informations des maîtres, c'est-à-dire l'ID et le nom du maître. Utilisez la propriété Page.Shapes pour déterminer quelle forme a été héritée par la forme de base.
### **Récupération de l'exemple de programmation des informations principales**
Le morceau de code suivant récupère les informations des maîtres à partir d'un diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-RetrieveMasterInfo-RetrieveMasterInfo.cs" >}}
## **Ajouter un maître à partir du gabarit de formes**
Un gabarit est une collection de formes associées à un gabarit particulier. Avec Aspose.Diagram, il est possible d'ajouter n'importe quel maître de forme à un dessin à partir d'un pochoir.
### **Ajouter maître**
 La[Maître](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'objet représente un[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maître de l'objet dans un diagram. La méthode AddMaster, exposée par la classe Diagram, permet d'ajouter un maître à partir d'un gabarit. Il propose les quatre manières suivantes :

- Chemin d'accès au fichier Stencil et ID principal.
- Chemin d'accès au fichier Stencil et nom du masque.
- Flux de fichiers Stencil et ID maître.
- Flux de fichier Stencil et nom du maître.
- Ajouter le maître à diagram à partir de la source diagram
#### **Ajouter un exemple de programmation maître**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-AddMasterFromStencil-AddMasterFromStencil.cs" >}}
## **Créer un maître à partir de zéro**
 Aspose.Diagram API permet de créer un[Maître](http://www.aspose.com/api/net/diagram/aspose.diagram/master) à partir de zéro sans aucun pochoir, dessin ou modèle. Les développeurs peuvent personnaliser la création de Master. La méthode AddMaster, exposée par la classe Diagram, permet d'ajouter un maître.
### **Créer un exemple de programmation maître**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateMasterFromScratch-CreateMasterFromScratch.cs" >}}
## **Obtenir un Master à partir du fichier Visio**
Parfois, les développeurs ont besoin d'obtenir les détails d'un maître de dessin Visio. Le Aspose.Diagram API prend en charge cette fonctionnalité.

 Aspose.Diagram for .NET offre le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)classe qui représente un dessin Visio. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour récupérer les détails d'un maître particulier. La classe MasterCollection expose les méthodes GetMasterByName et GetMaster qui peuvent être appelées pour obtenir un objet Master.
### **Obtenir un objet principal par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetMaster de la classe Diagram.Masters.
#### **Exemple de programmation d'objet maître par ID**
L'exemple suivant montre comment obtenir une forme de base par ID à partir d'un dessin Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyID-GetMasterbyID.cs" >}}
### **Obtenir un objet principal par nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetMasterByName de la classe Diagram.Masters.
#### **Exemple de programmation d'objet maître par nom**
L'exemple suivant montre comment obtenir un objet principal par son nom à partir d'un dessin Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyName-GetMasterbyName.cs" >}}
## **Vérifier la présence d'un maître dans le dessin Visio**
Le Aspose.Diagram API prend en charge la vérification de la présence d'un maître dans un dessin Visio. Avec la propriété MasterCollection, les développeurs peuvent vérifier si un maître est présent par son nom ou son ID.

 Aspose.Diagram for .NET offre le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe qui représente un dessin Visio. La propriété Masters, exposée par la classe Diagram, prend en charge une collection d'objets Aspose.Diagram.Master. Cette propriété peut être utilisée pour vérifier la présence d'un maître particulier. La classe MasterCollection expose la méthode IsExist qui peut être appelée avec le nom principal ou le paramètre ID.
### **Vérifier la présence d'un maître par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode IsExist de la classe Diagram.Masters.
#### **Présence principale par exemple de programmation ID**
L'exemple suivant montre comment vérifier la présence d'un maître par ID dans un dessin Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.cs" >}}
### **Vérifier la présence d'un maître par son nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode IsExist de la classe Diagram.Masters.
#### **Exemple de programmation de présence principale par nom**
L'exemple suivant montre comment vérifier la présence d'un maître par son nom à partir du dessin Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.cs" >}}
