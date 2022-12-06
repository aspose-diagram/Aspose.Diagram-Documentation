---
title: Abrufen, Abrufen, Kopieren und Einfügen einer Seite
type: docs
weight: 10
url: /de/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Abrufen von Seiteninformationen**
In Microsoft Visio sind Seiten entweder Vorder- oder Hintergrundseiten. Um Seiteninformationen zu erhalten, z. B. Seiten-ID und Seitenname, stellen Sie zunächst fest, ob es sich bei einer Seite um eine Hintergrund- oder eine Vordergrundseite handelt.

Das Objekt `Page` repräsentiert den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite. Die Pages-Eigenschaft, die von der `Diagram`-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Page-Objekten. Diese Eigenschaft kann verwendet werden, um Seiteninformationen abzurufen.

Verwenden Sie die Eigenschaft `Page.Background`, um zu bestimmen, ob eine Seite eine Vorder- oder Hintergrundseite ist.

### **Programmierbeispiel zum Abrufen von Seiteninformationen**
Der folgende Codeabschnitt ruft die Seiteninformationen von diagram ab.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-RetrievePageInfo.py" >}}

## **Rufen Sie die Visio-Seite von einer Diagram ab**
Manchmal müssen Entwickler die Seitendetails einer Visio-Zeichnung abrufen. Aspose.Diagram für Python über Java hat Funktionen, die ihnen dabei helfen.

Aspose.Diagram für Python über Java bietet die `Diagram`-Klasse, die eine Visio-Zeichnung darstellt. Die Pages-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von `Page`-Objekten. Die PageCollection-Klasse macht die `getPage`-Methode verfügbar, die aufgerufen werden kann, um das Page-Objekt abzurufen.

### **Abrufen eines Visio-Seitenobjekts nach ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die Methode getPage der Klasse Diagram.Pages auf.

Das folgende Beispiel zeigt, wie ein Seitenobjekt anhand der ID aus der Zeichnung Visio abgerufen wird.

#### **Programmierbeispiel zum Abrufen des Seitenobjekts nach ID**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyID.py" >}}

### **Abrufen eines Visio-Seitenobjekts nach Name**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetPage-Methode der Diagram.Pages-Klasse auf.

#### **Programmierbeispiel zum Abrufen des Seitenobjekts nach Namen**
Das folgende Beispiel zeigt, wie ein Seitenobjekt anhand des Namens aus der Zeichnung Visio abgerufen wird.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyName.py" >}}

## **Kopieren Sie eine Visio-Seite in eine andere Diagram-Seite**
Aspose.Diagram für Python über Java API ermöglicht es Entwicklern, den Inhalt von Visio diagram zu kopieren und zu einem anderen hinzuzufügen. In diesem Hilfethema wird erläutert, wie Sie diese Aufgabe ausführen.

Aspose.Diagram für Python über Java API hat die `Diagram`-Klasse, die eine Visio-Zeichnung darstellt. Die Pages-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von `Page`-Objekten. Die PageCollection-Klasse macht die `add`-Methode verfügbar, die aufgerufen werden kann, um ein weiteres Page-Objekt hinzuzufügen.

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein neues Objekt der Klasse Diagram.
1. Laden Sie ein vorhandenes Visio diagram in das Klassenobjekt Diagram.
1. Fügen Sie alle Master aus dem geladenen Visio diagram hinzu
1. Holen Sie sich das Seitenobjekt aus dem geladenen diagram (das kopiert werden muss).
1. Legen Sie den Namen und die ID des Seitenobjekts fest.
1. Leerseite der neuen diagram entfernen (optional).
1. Rufen Sie die add-Methode der PageCollection-Klasse auf.
1. Speichern Sie die neue diagram im Computerspeicher.

### **Kopieren Sie ein Programmierbeispiel für die Seite Visio**
Das folgende Codebeispiel zeigt, wie Sie ein Visio-Seitenobjekt in eine andere Visio-Zeichnung kopieren.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-CopyVisioPage.py" >}}

## **Kopieren Sie die Seite Visio in eine andere Seiteninstanz**
Die Methode `copy` der Klasse `Page` nimmt eine Seiteninstanz zum Klonen.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Einfügen einer leeren Seite in eine Visio-Zeichnung**
Aspose.Diagram für Python über Java kann eine neue leere Seite in die Zeichnung Microsoft Office Visio einfügen. In diesem Beispielthema wird beschrieben, wie Sie dies tun.

Die `add`-Methode, die von der Pages-Auflistung bereitgestellt wird, ermöglicht es Entwicklern, eine neue leere Seite in Visio diagram hinzuzufügen. Die Seiten-ID sollte zugewiesen werden.

### **Programmierbeispiel für eine leere Seite einfügen**
Der folgende Codeabschnitt fügt eine leere Seite in die Zeichnung Visio ein:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-InsertBlankPageInVisio.py" >}}

## **Seitenposition in der Zeichnung Visio verschieben**
Aspose.Diagram für Python über Java API kann die Seitenposition in der Visio-Zeichnung verschieben. Die `moveTo`-Methode, die von der `Page`-Klasse verfügbar gemacht wird, hilft Entwicklern, die Seitenposition zu verschieben.

### **Verschieben der Seitenposition Programmierbeispiel**
Das MoveTo-Member verwendet den Index der Zielseite als Parameter, um die Position der Seite in der Zeichnung Visio zu verschieben:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
