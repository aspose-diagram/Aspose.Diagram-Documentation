---
title: Travailler avec l'impression
type: docs
weight: 80
url: /fr/java/working-with-print/
---
## **Impression d'un Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) fournit quatre méthodes de surcharge pour l'impression des diagrammes. Ces méthodes sont suffisamment flexibles pour imprimer le diagram sur l'imprimante par défaut ou sur l'une des imprimantes disponibles avec des paramètres personnalisés. Il vous suffit de sélectionner la méthode d'impression appropriée en fonction des besoins.
### **Impression sur une imprimante spécifique**
L'impression du diagram sur l'imprimante spécifique nécessite le nom de l'imprimante comme paramètre de la méthode d'impression du Diagram. Effectuez les étapes suivantes afin d'imprimer le diagram sur l'imprimante souhaitée :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print de la classe Diagram avec le nom de l'imprimante comme paramètre de chaîne à la méthode Print
#### **Impression sur un exemple de programmation d'imprimante spécifique**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}

### **Définition de l'imprimante et du nom du document**
Aspose.Diagram Les API permettent de définir l'imprimante spécifique et le nom du document pour un travail d'impression. Effectuez les étapes suivantes afin d'imprimer le diagram sur l'imprimante souhaitée :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print de la classe Diagram avec l'imprimante et le nom du document comme paramètre de chaîne à la méthode Print
#### **Configuration de l'imprimante et du nom du document Exemple de programmation**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

