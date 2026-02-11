---
title: Récupérer, obtenir, copier et insérer une page
type: docs
weight: 10
url: /fr/net/retrieve-get-copy-and-insert-a-page/
description: Cette section explique comment insérer une page, copier une page ou obtenir des informations sur la page avec Aspose.Diagram.
---
## **Récupération des informations sur la page**
Dans Microsoft Visio, les pages sont soit des pages de premier plan, soit des pages d'arrière-plan. Pour obtenir des informations sur la page, par exemple l'ID de la page et le nom de la page, déterminez d'abord si une page est une page d'arrière-plan ou de premier plan.

 La[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page)L'objet représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Pages exposée par le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) prend en charge une collection d'objets Aspose.Diagram.Page. Cette propriété peut être utilisée pour récupérer des informations sur la page.

Utilisez la propriété Page.Background pour déterminer si une page est une page de premier plan ou d'arrière-plan .
### **Récupérer un exemple de programmation d'informations sur la page**
Le morceau de code suivant récupère les informations de pages d'un diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}
```
## **Obtenez la page Visio d'un Diagram**
Parfois, les développeurs doivent obtenir les détails de la page d'un dessin Visio. Aspose.Diagram a des fonctionnalités qui les aident à le faire.

 Aspose.Diagram for .NET offre le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe qui représente un dessin Visio. La propriété Pages exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Page. La classe PageCollection expose la méthode GetPage qui peut être appelée pour obtenir l'objet Page.
### **Obtenir un objet de page Visio par ID**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetPage de la classe Diagram.Pages.

L'exemple suivant montre comment obtenir un objet de page par ID à partir du dessin Visio.
#### **Obtenir un objet de page par ID Exemple de programmation**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}
```
### **Obtenir un objet de page Visio par nom**
Cet exemple fonctionne comme suit :

1. Créez un objet de la classe Diagram.
1. Appelez la méthode GetPage de la classe Diagram.Pages.
#### **Obtenir un objet de page par nom Exemple de programmation**
L'exemple suivant montre comment obtenir un objet de page par son nom à partir du dessin Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}
```
## **Copier une page Visio dans une autre Diagram**
Aspose.Diagram for .NET API permet aux développeurs de copier et d'ajouter son contenu d'un Visio diagram à un autre. Cette rubrique d'aide explique comment accomplir cette tâche.

 Aspose.Diagram for .NET API a le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe qui représente un dessin Visio. La propriété Pages exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Page. La classe PageCollection expose la méthode Add qui peut être appelée pour ajouter un autre objet Page.

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
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Copier la page Visio vers une autre instance de page**
La méthode Copy de la classe Page prend une instance de page à cloner.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Insérer une page vierge dans un dessin Visio**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) peut insérer une nouvelle page vierge dans le dessin Microsoft Office Visio. Cet exemple de rubrique décrit comment procéder.

La méthode Add, exposée par la collection Pages, permet aux développeurs d'ajouter une nouvelle page vierge dans le Visio diagram. L'ID de page doit être attribué.
### **Insérer un exemple de programmation de page vierge**
Le morceau de code suivant insère une page vierge dans le dessin Visio :

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Déplacer la position de la page dans le dessin Visio**
Aspose.Diagram for .NET API peut déplacer la position de la page dans le dessin Visio. La méthode MoveTo, exposée par la classe Page, aide les développeurs à déplacer la position de la page.
### **Déplacer la position de la page Exemple de programmation**
Le membre MoveTo prend l'index de la page cible comme paramètre pour déplacer la position de la page dans le dessin Visio :

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
