---
title: Récupérer, obtenir, copier et insérer une page
type: docs
weight: 10
url: /fr/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Récupération des informations sur la page**
Dans Microsoft Visio, les pages sont soit des pages de premier plan, soit des pages d'arrière-plan. Pour obtenir des informations sur la page, par exemple l'ID de la page et le nom de la page, déterminez d'abord si une page est une page d'arrière-plan ou de premier plan.

L'objet `Page` représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Pages exposée par la classe `Diagram` prend en charge une collection d'objets Page. Cette propriété peut être utilisée pour récupérer des informations sur la page.

Utilisez la propriété `Page.Background` pour déterminer si une page est une page de premier plan ou d'arrière-plan.

### **Récupérer un exemple de programmation d'informations sur la page**
Le morceau de code suivant récupère les informations de pages d'un diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-RetrievePageInfo.py" >}}

## **Obtenez la page Visio d'un Diagram**
Parfois, les développeurs doivent obtenir les détails de la page d'un dessin Visio. Aspose.Diagram pour Python via Java a des fonctionnalités qui les aident à le faire.

Aspose.Diagram pour Python via Java propose la classe `Diagram` qui représente un dessin Visio. La propriété Pages exposée par la classe Diagram prend en charge une collection d'objets `Page`. La classe PageCollection expose la méthode `getPage` qui peut être appelée pour obtenir l'objet Page.

### **Obtenir un objet de page Visio par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode getPage de la classe Diagram.Pages.

L'exemple suivant montre comment obtenir un objet de page par ID à partir du dessin Visio.

#### **Obtenir un objet de page par ID Exemple de programmation**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyID.py" >}}

### **Obtenir un objet de page Visio par nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetPage de la classe Diagram.Pages.

#### **Obtenir un objet de page par nom Exemple de programmation**
L'exemple suivant montre comment obtenir un objet de page par son nom à partir du dessin Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyName.py" >}}

## **Copier une page Visio dans une autre Diagram**
Aspose.Diagram pour Python via Java API permet aux développeurs de copier et d'ajouter son contenu d'un Visio diagram à un autre. Cette rubrique d'aide explique comment accomplir cette tâche.

Aspose.Diagram pour Python via Java API a la classe `Diagram` qui représente un dessin Visio. La propriété Pages exposée par la classe Diagram prend en charge une collection d'objets `Page`. La classe PageCollection expose la méthode `add` qui peut être appelée pour ajouter un autre objet Page.

Cet exemple fonctionne comme suit :

1. Créez un nouvel objet de la classe Diagram.
1. Chargez un Visio diagram existant dans l'objet de classe Diagram.
1. Ajouter tous les maîtres du Visio chargé diagram
1. Obtenez l'objet de page à partir du diagram chargé (qui doit être copié).
1. Définissez le nom et l'identifiant de l'objet de la page.
1. Supprimer la page vide du nouveau diagram (facultatif).
1. Appelez la méthode add de la classe PageCollection.
1. Enregistrez le nouveau diagram dans la mémoire de l'ordinateur.

### **Copier un exemple de programmation de page Visio**
L'exemple de code ci-dessous montre comment copier un objet de page Visio dans un autre dessin Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-CopyVisioPage.py" >}}

## **Copier la page Visio vers une autre instance de page**
La méthode `copy` de la classe `Page` prend une instance de page à cloner.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Insérer une page vierge dans un dessin Visio**
Aspose.Diagram pour Python via Java peut insérer une nouvelle page vierge dans le dessin Microsoft Office Visio. Cet exemple de rubrique décrit comment procéder.

La méthode `add`, exposée par la collection Pages, permet aux développeurs d'ajouter une nouvelle page vierge dans le Visio diagram. L'ID de page doit être attribué.

### **Insérer un exemple de programmation de page vierge**
Le morceau de code suivant insère une page vierge dans le dessin Visio :

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-InsertBlankPageInVisio.py" >}}

## **Déplacer la position de la page dans le dessin Visio**
Aspose.Diagram pour Python via Java API peut déplacer la position de la page dans le dessin Visio. La méthode `moveTo`, exposée par la classe `Page`, aide les développeurs à déplacer la position de la page.

### **Déplacer la position de la page Exemple de programmation**
Le membre MoveTo prend l'index de la page cible comme paramètre pour déplacer la position de la page dans le dessin Visio :

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
