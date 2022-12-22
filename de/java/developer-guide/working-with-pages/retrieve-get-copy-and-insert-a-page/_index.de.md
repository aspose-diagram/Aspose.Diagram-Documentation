---
title: Abrufen, Abrufen, Kopieren und Einfügen einer Seite
type: docs
weight: 10
url: /de/java/retrieve-get-copy-and-insert-a-page/
---
## **Abrufen von Seiteninformationen**
In Microsoft Visio sind Seiten entweder Vorder- oder Hintergrundseiten. Um Seiteninformationen zu erhalten, z. B. Seiten-ID und Seitenname, stellen Sie zunächst fest, ob es sich bei einer Seite um eine Hintergrund- oder eine Vordergrundseite handelt.

 Das[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Die Pages-Eigenschaft, die von der[Diagram](https://reference.aspose.com/diagram/java) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten. Diese Eigenschaft kann verwendet werden, um Seiteninformationen abzurufen.

Verwenden Sie die Page.Background-Eigenschaft, um zu bestimmen, ob eine Seite eine Vorder- oder Hintergrundseite ist.

Das folgende Bild zeigt die Ausgabe der Codeausschnitte in diesem Artikel.

**Eine Konsole, die die Ausgabe anzeigt.** 

![todo: Bild_alt_Text](retrieve-get-copy-and-insert-a-page_1.png)
### **Programmierbeispiel zum Abrufen von Seiteninformationen**
Der folgende Codeabschnitt ruft die Seiteninformationen von diagram ab.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-RetrievePageInfo-RetrievePageInfo.java" >}}
## **Rufen Sie die Visio-Seite von einer Diagram ab**
Manchmal müssen Entwickler die Seitendetails einer Visio-Zeichnung abrufen. Aspose.Diagram hat Funktionen, die ihnen dabei helfen.

 Aspose.Diagram for Java bietet die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Die Pages-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten. Die PageCollection-Klasse macht die GetPage-Methode verfügbar, die zum Abrufen des Page-Objekts aufgerufen werden kann.
### **Abrufen eines Visio-Seitenobjekts nach ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetPage-Methode der Diagram.Pages-Klasse auf.

Das folgende Beispiel zeigt, wie ein Seitenobjekt anhand der ID aus der Zeichnung Visio abgerufen wird.
#### **Programmierbeispiel zum Abrufen des Seitenobjekts nach ID**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyID-GetVisioPagebyID.java" >}}
### **Abrufen eines Visio-Seitenobjekts nach Name**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetPage-Methode der Diagram.Pages-Klasse auf.
#### **Programmierbeispiel zum Abrufen des Seitenobjekts nach Namen**
Das folgende Beispiel zeigt, wie ein Seitenobjekt anhand des Namens aus der Zeichnung Visio abgerufen wird.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyName-GetVisioPagebyName.java" >}}
## **Kopieren Sie eine Visio-Seite in eine andere Diagram-Seite**
Aspose.Diagram for Java API ermöglicht es Entwicklern, den Inhalt von einer Visio diagram zu einer anderen zu kopieren und hinzuzufügen. In diesem Hilfethema wird erläutert, wie Sie diese Aufgabe ausführen.

 Aspose.Diagram for Java API hat die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Die Pages-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten. Die PageCollection-Klasse macht die Add-Methode verfügbar, die aufgerufen werden kann, um ein weiteres Page-Objekt hinzuzufügen.

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein neues Objekt der Klasse Diagram.
1. Laden Sie ein vorhandenes Visio diagram in das Klassenobjekt Diagram.
1. Fügen Sie alle Master aus dem geladenen Visio diagram hinzu
1. Holen Sie sich das Seitenobjekt aus dem geladenen diagram (das kopiert werden muss).
1. Legen Sie den Namen und die ID des Seitenobjekts fest.
1. Leerseite der neuen diagram entfernen (optional).
1. Rufen Sie die Add-Methode der PageCollection-Klasse auf.
1. Speichern Sie die neue diagram im Computerspeicher.
### **Kopieren Sie ein Programmierbeispiel für die Seite Visio**
Das folgende Codebeispiel zeigt, wie Sie ein Visio-Seitenobjekt in eine andere Visio-Zeichnung kopieren.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-CopyVisioPage-CopyVisioPage.java" >}}
## **Kopieren Sie die Seite Visio in eine andere Seiteninstanz**
Die Copy-Methode der Page-Klasse nimmt eine Seiteninstanz zum Klonen.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Einfügen einer leeren Seite in eine Visio-Zeichnung**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) kann eine neue leere Seite in die Zeichnung Microsoft Office Visio einfügen. In diesem Beispielthema wird beschrieben, wie Sie dies tun.

Die Add-Methode, die von der Pages-Auflistung bereitgestellt wird, ermöglicht es Entwicklern, eine neue leere Seite in Visio diagram hinzuzufügen. Die Seiten-ID sollte zugewiesen werden.
### **Programmierbeispiel für eine leere Seite einfügen**
Der folgende Codeabschnitt fügt eine leere Seite in die Zeichnung Visio ein:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.java" >}}
## **Seitenposition in der Zeichnung Visio verschieben**
Aspose.Diagram for Java API kann die Seitenposition in der Visio Zeichnung verschieben. Die moveTo-Methode, die von der Page-Klasse verfügbar gemacht wird, hilft Entwicklern, die Seitenposition zu verschieben.
### **Verschieben der Seitenposition Programmierbeispiel**
Das MoveTo-Member verwendet den Index der Zielseite als Parameter, um die Position der Seite in der Zeichnung Visio zu verschieben:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
