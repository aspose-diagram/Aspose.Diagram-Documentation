---
title: Obtenir Visio Shape Inherit Chars
type: docs
weight: 101
url: /fr/java/get-visio-shape-inherit-chars/
description: Cette section explique comment obtenir le style de police de la forme visio hérité de son style parent et maître avec Aspose.Diagram.
---
### **Récupérer les données de police héritées d'une forme Visio**
 Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir ou définir les données de police héritées d'une forme Visio. La propriété InheritChars, exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) classe, contient les valeurs de police pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de police héritées**
L'extrait de code suivant récupère les données de police héritées de la forme. Veuillez vérifier cet exemple de code :

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedChars.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Chars from the parent style and master
CharCollection chars = shape.getInheritChars();
for (int j = 0; j < chars.getCount(); j++) 
{
	Char ch = chars.get(j);
	System.out.println(ch.getColor().getValue());
	System.out.println(ch.getColorTrans().getValue());
	System.out.println(ch.getFontScale().getValue());
	System.out.println(ch.getSize().getValue());
	System.out.println(ch.getStyle().getValue());
	System.out.println(ch.getFontName().getValue());
	System.out.println(ch.isBold());
	System.out.println(ch.isDoubleStrikethrough());
	System.out.println(ch.isDoubleUnderline());
	System.out.println(ch.isItalic());
	System.out.println(ch.isStrikethrough());
	System.out.println(ch.isSubscript());
	System.out.println(ch.isSuperscript());
	System.out.println(ch.isUnderline());
}

{{< /highlight >}}
```



