---
title: Travailler avec du texte
type: docs
weight: 120
url: /fr/java/working-with-text/
---
## **Insérer une forme de texte dans la page Visio**
 Aspose.Diagram API permet aux développeurs d'insérer une forme de texte n'importe où dans la page Visio. Pour ce faire, la méthode addText de la[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) La classe prend les paramètres PinX, PinY, largeur, hauteur et texte.
### **Insérer un exemple de programmation de forme de texte**
Le morceau de code suivant ajoute une forme de texte dans le Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertTextShape.class) + "Text/";
// create a new diagram
Diagram diagram = new Diagram();
// set parameters
double PinX = 1, PinY = 1, Width = 1, Height = 1;
String text = "Test text";
// add text to a Visio page
diagram.getPages().getPage(0).addText(PinX, PinY, Width, Height, text);
// save diagram 
diagram.save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Mise à jour Visio Texte de forme**
 Aussi bien que[création de diagrammes](/diagram/fr/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java vous permet de travailler avec des formes de différentes manières. Cet article explique comment accéder au texte et le mettre à jour dans les formes.

 La propriété Text, exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) classe, prend en charge l'objet Aspose.Diagram.Text. La propriété peut être utilisée pour récupérer ou mettre à jour le texte d'une forme.

**Entrée diagram** 

![tâche : image_autre_texte](http://i.imgur.com/6aEp7h0.png)

**Diagram après que le texte de la forme centrale est passé de Traiter à Nouveau texte** 

![tâche : image_autre_texte](http://i.imgur.com/o977cxw.png)

Le processus de mise à jour du texte d'une forme est simple :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Définissez le nouveau texte.
1. Enregistrez le diagram.
### **Mise à jour de l'exemple de programmation de texte de forme**
Le morceau de code suivant met à jour le texte d'une forme. Les formes sont identifiées par leurs identifiants. Les segments de code ci-dessous recherchent une forme appelée processus et avec l'ID 1 et modifient son texte.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UpdateShapeText.class); 
//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find a particular shape and update its text
for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getText().getValue().clear();
        shape.getText().getValue().add(new Txt("New Text"));
    }
}
// save diagram
diagram.save(dataDir + "UpdateShapeText_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Appliquer une feuille de style intégrée ou personnalisée à une forme Visio**
Les feuilles de style Microsoft Visio stockent les informations de mise en forme qui peuvent être appliquées aux formes pour une apparence cohérente. Aspose.Diagram for Java vous permet d'appliquer des feuilles de style depuis l'intérieur d'une application.

 Les propriétés TextStyle, FillStyle et LineStyle exposées par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) soutenir la classe[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) objet. La propriété peut être utilisée pour récupérer des informations de style et appliquer des styles de texte, de ligne et de remplissage personnalisés à un diagram.

**Entrée diagram** 

![tâche : image_autre_texte](http://i.imgur.com/feV1x2N.png)

**Le diagram après avoir appliqué une feuille de style personnalisée qui définit les styles de texte, de ligne et de remplissage** 

![tâche : image_autre_texte](http://i.imgur.com/Xk9W0wN.png)
### **Styles personnalisés dans Microsoft Visio**
Pour appliquer des styles personnalisés aux formes dans Microsoft Visio :

1. Ouvrez un diagram au Microsoft Visio.
1.  Sélectionner**Définir les styles** du**Format** menu (Visio 2007), ou clic droit**modes** dans le**Explorateur de dessins** fenêtre et sélectionnez**Définir les styles** (Visio 2010).
1.  Dans le**Définir les styles** boîte de dialogue, saisissez un nouveau nom pour votre feuille de style personnalisée. Par exemple, CustomStyle1.
1.  Clique le**Texte**, **Ligne** et**Remplir** boutons pour définir respectivement les styles de texte, de ligne et de remplissage.
1.  Cliquez sur**D'ACCORD**.

Après avoir défini des feuilles de style personnalisées dans Microsoft Visio, utilisez le code suivant dans une application Java pour appliquer des styles personnalisés à vos formes. Notez que les exemples de code ci-dessous appellent la feuille de style personnalisée définie ci-dessus : vous devez connaître le nom et l'emplacement de la feuille que vous appliquez.

Pour appliquer des styles personnalisés par programmation :

1. Charger un diagram.
1. Recherchez la forme à laquelle vous souhaitez appliquer un style.
1. Chargez la feuille de style.
1. Appliquer des styles.
1. Enregistrez le diagram.
#### **Appliquer un exemple de programmation de styles personnalisés**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyCustomStyleSheets.class);

//Load diagram
Diagram diagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
Shape sourceShape = null;
        
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find the shape that you want to apply style to
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process") {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

//Find the required style sheet
for (StyleSheet styleSheet : (Iterable<StyleSheet>) diagram.getStyleSheets())
{
    if (styleSheet.getName() == "CustomStyle1")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    //Apply text style
    sourceShape.setTextStyle(customStyleSheet);
    //Apply fill style
    sourceShape.setFillStyle(customStyleSheet);
    //Apply line style
    sourceShape.setLineStyle(customStyleSheet);
}

 //Save the changed diagram as VDX
diagram.save(dataDir + "ApplyCustomStyleSheets_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Appliquer un style différent sur chaque valeur de texte d'une forme**
 Aussi bien que[création de diagrammes](/diagram/fr/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java vous permet de travailler avec des formes de différentes manières. Cet article vous aide à ajouter plusieurs valeurs de texte à une forme et à appliquer un style différent à chaque valeur de texte.

{{% alert color="primary" %}} 

L'élément Shape contient un élément appelé Text, qui contient les caractères du texte et des éléments spéciaux (cp, pp, tp et fld) qui marquent la fin d'une exécution et le début de la suivante. Char Element contient les attributs de mise en forme du texte de la forme, tels que la police, la couleur, le style de texte, la casse, la position par rapport à la ligne de base et la taille en points.

{{% /alert %}} 
### **Ajout de texte et de styles de forme**
**Entrée diagram** 

![tâche : image_autre_texte](http://i.imgur.com/ZqgQPQC.png)

**Diagram après avoir ajouté diverses valeurs de texte à une forme avec un style différent sur chaque valeur de texte** 

![tâche : image_autre_texte](http://i.imgur.com/7UWhFbU.png)
#### **Exemple de programmation d'ajout de texte et de styles**
Le morceau de code suivant ajoute le texte d'une forme et différents styles.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyFontOnText.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// clear shape text values and chars
shape.getText().getValue().clear();
shape.getChars().clear();

// mark character run and add text
shape.getText().getValue().add(new Cp(0));
shape.getText().getValue().add(new Txt("TextStyle_Regular\n"));
shape.getText().getValue().add(new Cp(1));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic\n"));
shape.getText().getValue().add(new Cp(2));
shape.getText().getValue().add(new Txt("TextStyle_Underline_Italic\n"));
shape.getText().getValue().add(new Cp(3));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic_Underline"));

// add formatting characters
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());

//set properties e.g. color, font, size and style etc.
shape.getChars().get(0).setIX(0);
shape.getChars().get(0).getColor().setValue("#FF0000");
shape.getChars().get(0).getFont().setValue(1);
shape.getChars().get(0).getSize().setValue(0.22);
shape.getChars().get(0).getStyle().setValue(StyleValue.UNDEFINED);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(1).setIX(1);
shape.getChars().get(1).getColor().setValue("#FF00FF");
shape.getChars().get(1).getFont().setValue(1);
shape.getChars().get(1).getSize().setValue(0.22);
shape.getChars().get(1).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(2).setIX(2);
shape.getChars().get(2).getColor().setValue("#00FF00");
shape.getChars().get(2).getFont().setValue(1);
shape.getChars().get(2).getSize().setValue(0.22);
shape.getChars().get(2).getStyle().setValue(StyleValue.UNDERLINE | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(3).setIX(3);
shape.getChars().get(3).getColor().setValue("#3333FF");
shape.getChars().get(3).getFont().setValue(1);
shape.getChars().get(3).getSize().setValue(0.22);
shape.getChars().get(3).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC | StyleValue.UNDERLINE);
// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Rechercher et remplacer le texte d'une forme**
 La[SMS](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) La classe vous permet de modifier le texte de la forme. La méthode Replace, exposée par le[SMS](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) classe, prend en charge la modification du texte d'une forme.
Les exemples de code de cet article recherchent et remplacent le texte de la forme sur la page.

**Entrée diagram** 

![tâche : image_autre_texte](http://i.imgur.com/lW5xaP0.png)


**Le diagram après la modification de la forme** 

![tâche : image_autre_texte](http://i.imgur.com/m33W1Tk.png)

Le processus de modification du texte de la forme :

1. Charger un diagram.
1. Trouver un texte particulier d'une forme.
1. Remplacer le texte de cette forme
1. Enregistrez le diagram.
### **Rechercher et remplacer un exemple de programmation de texte**
Les extraits de code ci-dessous montrent comment modifier le texte de la forme. Le code parcourt les formes d'une page.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(FindAndReplaceShapeText.class); 
// load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");

DateFormat dateFormat = new SimpleDateFormat("dd/MMMM/yyyy");
Date myDate = new Date(System.currentTimeMillis());
Calendar cal = Calendar.getInstance();

// Prepare a collection old and new text
Hashtable<String, String> replacements = new Hashtable<String, String>();
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[EmplyeeName]]", "James Bond");
replacements.put("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");

cal.setTime(myDate);
cal.add(Calendar.YEAR, -1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[TimePeriod]]", dateFormat.format(cal.getTime()) + " -- " + dateFormat.format(myDate));

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, -7);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[SubmissionDate]]", dateFormat.format(cal.getTime()));
replacements.put("[[AmountReq]]", "$100,000");

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, 1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[DateApproved]]", dateFormat.format(cal.getTime()));

// Iterate through the shapes of a page
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    Set<String> keys = replacements.keySet();
    for(String key: keys)
    {
        for (FormatTxt txt : (Iterable<FormatTxt>) shape.getText().getValue())
        {
       	    Txt tx = (Txt)((txt instanceof Txt) ? txt : null);
            if (tx != null && tx.getText().contains(key))
            {
                //find and replace text of a shape
                tx.setText(tx.getText().replace(key, replacements.get(key)));
            }
        }
    }
}
// Save the diagram
diagram.save(dataDir + "FindAndReplaceShapeText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Extraire le texte brut de la page Visio Diagram**
Aspose.Diagram API permet aux développeurs d'extraire du texte brut de la page Visio diagram. Ils peuvent également parcourir les pages Visio diagram pour couvrir l'ensemble du texte Visio diagram.

 Microsoft Office Visio ajoute le texte aux formes. La[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe contient un élément appelé Text, qui contient les caractères du texte et des éléments spéciaux (cp, pp, tp et fld) qui marquent la fin d'une exécution et le début de la suivante.
### **Extraire un exemple de programmation en texte brut**
Le morceau de code suivant parcourt les formes de la page Visio et filtre le texte brut sans formater les informations.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
static String text = "";
public static void main(String[] args) throws Exception
{
       // The path to the documents directory.
       String dataDir = Utils.getDataDir(GetPlainTextOfVisio.class);
       // load diagram
       Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

       // get Visio diagram page
       Page page = diagram.getPages().getPage("Page-1");

       // iterate through the shapes
       for (Shape shape :(Iterable<Shape>) page.getShapes())
       {
           // extract plain text from the shape
           GetShapeText(shape);
       }
       // display extracted text
       System.out.println(text);
}
   private static void GetShapeText(Shape shape)
   {
   	// filter shape text
       if (shape.getText().getValue().getText() != "")
       	text += (shape.getText().getValue().getText().replaceAll("\\<.*?>",""));

       // for image shapes
       if (shape.getType() == TypeValue.FOREIGN)
           text += (shape.getName());

       // for group shapes
       if (shape.getType() == TypeValue.GROUP)
           for(Shape subshape : (Iterable<Shape>) shape.getShapes())
           {
               GetShapeText(subshape);
           }
   }

{{< /highlight >}}
```
