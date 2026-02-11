---
title: Récupérer, obtenir, copier et insérer une page
type: docs
weight: 10
url: /fr/java/retrieve-get-copy-and-insert-a-page/
---
## **Récupération des informations sur la page**
Dans Microsoft Visio, les pages sont soit des pages de premier plan, soit des pages d'arrière-plan. Pour obtenir des informations sur la page, par exemple l'ID de la page et le nom de la page, déterminez d'abord si une page est une page d'arrière-plan ou de premier plan.

 La[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)L'objet représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Pages exposée par le[Diagram](https://reference.aspose.com/diagram/java) prend en charge une collection d'objets Aspose.Diagram.Page. Cette propriété peut être utilisée pour récupérer des informations sur la page.

Utilisez la propriété Page.Background pour déterminer si une page est une page de premier plan ou d'arrière-plan .

L'image ci-dessous montre la sortie des extraits de code de cet article.

**Une console montrant la sortie.** 

![tâche : image_autre_texte](retrieve-get-copy-and-insert-a-page_1.png)
### **Récupérer un exemple de programmation d'informations sur la page**
Le morceau de code suivant récupère les informations de pages d'un diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrievePageInfo.class);

//Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrievePageInfo.vdx");

for (Page page : (Iterable<Page>) diagram.getPages())
{
    //Checks if current page is a background page
    if (page.getBackground() == com.aspose.diagram.BOOL.TRUE)
    {
        //Display information about the background page
        System.out.println("Background Page ID : " + page.getID());
        System.out.println("Background Page Name : " + page.getName());
    }
    else
    {
        //Display information about the foreground page
        System.out.println("\nPage ID : " + page.getID());
        System.out.println("Universal Name : " + page.getNameU());
        System.out.println("ID of the Background Page : " + page.getBackPage());
    }
}

{{< /highlight >}}
```
## **Obtenez la page Visio d'un Diagram**
Parfois, les développeurs doivent obtenir les détails de la page d'un dessin Visio. Aspose.Diagram a des fonctionnalités qui les aident à le faire.

 Aspose.Diagram for Java offre le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe qui représente un dessin Visio. La propriété Pages exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Page. La classe PageCollection expose la méthode GetPage qui peut être appelée pour obtenir l'objet Page.
### **Obtenir un objet de page Visio par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetPage de la classe Diagram.Pages.

L'exemple suivant montre comment obtenir un objet de page par ID à partir du dessin Visio.
#### **Obtenir un objet de page par ID Exemple de programmation**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyID.class); 
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.getPages().getPage(pageid);

{{< /highlight >}}
```
### **Obtenir un objet de page Visio par nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetPage de la classe Diagram.Pages.
#### **Obtenir un objet de page par nom Exemple de programmation**
L'exemple suivant montre comment obtenir un objet de page par son nom à partir du dessin Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyName.class);     
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
String pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.getPages().getPage(pageName);

{{< /highlight >}}
```
## **Copier une page Visio dans une autre Diagram**
Aspose.Diagram for Java API permet aux développeurs de copier et d'ajouter son contenu d'un Visio diagram à un autre. Cette rubrique d'aide explique comment accomplir cette tâche.

 Aspose.Diagram for Java API a le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe qui représente un dessin Visio. La propriété Pages exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Page. La classe PageCollection expose la méthode Add qui peut être appelée pour ajouter un autre objet Page.

Cet exemple fonctionne comme suit :

1. Créez un nouvel objet de la classe Diagram.
1. Chargez un Visio diagram existant dans l'objet de classe Diagram.
1. Ajouter tous les maîtres du Visio chargé diagram
1. Obtenez l'objet de page à partir du diagram chargé (qui doit être copié).
1. Définissez le nom et l'identifiant de l'objet de la page.
1. Supprimer la page vide du nouveau diagram (facultatif).
1. Appelez la méthode Add de la classe PageCollection.
1. Enregistrez le nouveau diagram dans la mémoire de l'ordinateur.
### **Copier un exemple de programmation de page Visio**
L'exemple de code ci-dessous montre comment copier un objet de page Visio dans un autre dessin Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyVisioPage.class);
        
// Call the diagram constructor to load diagram from a VSD file
Diagram originalDiagram = new Diagram(dataDir + "Drawing1.vsd");

// initialize the new visio diagram
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = originalDiagram.getMasters();
for (Master master : (Iterable<Master>) originalMasters) {
   newDiagram.addMaster(originalDiagram, master.getName());
}

// get the page object from the original diagram
Page SrcPage = originalDiagram.getPages().getPage("Page-1");
// set page name
SrcPage.setName("new page");
        
// it calculates max page id
int max = 0;
if (newDiagram.getPages().getCount() != 0)
    max = newDiagram.getPages().get(0).getID();

for (int i = 1; i < newDiagram.getPages().getCount(); i++)
{
    if (max < newDiagram.getPages().get(i).getID())
        max = newDiagram.getPages().get(i).getID();
}
       
int MaxPageId = max;
// set page id
SrcPage.setID(MaxPageId);
// add reference of the original diagram page
newDiagram.getPages().add(SrcPage);

// remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0));

// save diagram in VDX format
newDiagram.save(dataDir + "CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Copier la page Visio vers une autre instance de page**
La méthode Copy de la classe Page prend une instance de page à cloner.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Insérer une page vierge dans un dessin Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) peut insérer une nouvelle page vierge dans le dessin Microsoft Office Visio. Cet exemple de rubrique décrit comment procéder.

La méthode Add, exposée par la collection Pages, permet aux développeurs d'ajouter une nouvelle page vierge dans le Visio diagram. L'ID de page doit être attribué.
### **Insérer un exemple de programmation de page vierge**
Le morceau de code suivant insère une page vierge dans le dessin Visio :

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(InsertBlankPageInVisio.class);   
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// it calculates max page id
int max = 0;
if (diagram.getPages().getCount() != 0)
    max = diagram.getPages().get(0).getID();

for (int i = 1; i < diagram.getPages().getCount(); i++)
{
    if (max < diagram.getPages().get(i).getID())
        max = diagram.getPages().get(i).getID();
}
        
// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.setName("new page");
// Set page ID
newPage.setID(max + 1);

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.getPages().add(newPage);

// Save diagram
diagram.save(dataDir + "InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Déplacer la position de la page dans le dessin Visio**
Aspose.Diagram for Java API peut déplacer la position de la page dans le dessin Visio. La méthode moveTo, exposée par la classe Page, aide les développeurs à déplacer la position de la page.
### **Déplacer la position de la page Exemple de programmation**
Le membre MoveTo prend l'index de la page cible comme paramètre pour déplacer la position de la page dans le dessin Visio :

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
