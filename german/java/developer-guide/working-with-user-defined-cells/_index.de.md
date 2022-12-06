---
title: Arbeiten mit benutzerdefinierten Zellen
type: docs
weight: 100
url: /de/java/working-with-user-defined-cells/
---
## **Benutzerdefinierte Zellen der Visio-Formen lesen**
 Benutzer fügen Textfelder in Formen ein, um zusätzliche Informationen anzuzeigen.**Benutzerdefinierte Zellen** ist die eine Verzweigung dieser Felder, und diese Verzweigung verwendet Informationen, die in die Wertzelle des Abschnitts Benutzerdefinierte Zellen im ShapeSheet des Shapes eingegeben wurden. Entwickler können alle benutzerdefinierten Zellen mit einfügen und lesen[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 Die Users-Auflistung, die von der bereitgestellt wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) -Klasse unterstützt das Objekt com.aspose.diagram.User. Das[Benutzer](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) Klasse kann zum Lesen von Eigenschaften verwendet werden. Es gibt einige benutzerdefinierte Zellen, wie Sie im folgenden Bild sehen können:

**Tabelle mit Informationen zu benutzerdefinierten Zellen** 

![todo: Bild_alt_Text](working-with-user-defined-cells_1.png)

Der folgende Code wird verwendet, um benutzerdefinierte Zellen zu lesen.

Das folgende Bild zeigt die Ausgabe nach dem Ausführen des Codes:

![todo: Bild_alt_Text](working-with-user-defined-cells_2.png)
#### **Programmierbeispiele**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.java" >}}
### **Benutzerdefinierte Zelle erstellen**
Mit Aspose.Diagram for Java API können Entwickler benutzerdefinierte Zellen im Shapesheet erstellen. In diesem Beispielthema wird beschrieben, wie Sie so viele Benutzernamenzeilen wie nötig hinzufügen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen.

Die add-Methode, die von der Users-Sammlung verfügbar gemacht wird, kann verwendet werden, um benutzerdefinierte Zellen im Shapesheet zu erstellen. Es dauert einen einzigen Parameter.

Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um eine benutzerdefinierte Zelle im Shapesheet mit Aspose.Diagram for Java zu erstellen.
#### **Programmierbeispiele**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
## **Benutzerdefinierte Zellen aus Shapesheet abrufen**
Aspose.Diagram for Java API ermöglicht es Entwicklern, benutzerdefinierte Zellen aus dem Shapesheet abzurufen. In diesem Beispielthema wird beschrieben, wie alle Benutzernamen für alle Shapes in einer Zeichnung abgerufen werden.
### **Benutzerdefinierte Zellen abrufen**
 Die Methoden getNameU(), getValue().getVal() und getPrompt().getValue(), die von der bereitgestellt werden[Benutzer](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)Klasse kann verwendet werden, um benutzerdefinierte Zellen aus dem Shapesheet abzurufen.
#### **Abrufen von Zellen aus Shapesheet-Programmierbeispielen**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um alle benutzerdefinierten Zellen aus dem Shapesheet mit Aspose.Diagram for Java abzurufen.
#### **Programmierbeispiele**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
