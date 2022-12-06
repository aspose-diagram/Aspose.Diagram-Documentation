---
title: Arbeiten mit Meistern
type: docs
weight: 70
url: /de/net/working-with-masters/
description: In diesem Abschnitt wird erläutert, wie Sie mit Aspose.Diagram Master hinzufügen oder Masterinformationen abrufen.
---
## **Stammdaten abrufen**
Ein Shape-Master ist ein anderer Name für eine Visio-Schablone. Mit Aspose.Diagram können Informationen über Seiten, Konnektoren und auch Master abgerufen werden. Dieser Artikel erklärt, wie Sie die ID und den Namen von einer diagram erhalten.

 Das[Meister](http://www.aspose.com/api/net/diagram/aspose.diagram/master) Objekt repräsentiert a[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Master-Objekt in einem diagram. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um die Informationen des Masters abzurufen, d. h. die Master-ID und den Namen. Verwenden Sie die Page.Shapes-Eigenschaft, um zu bestimmen, welche Form von der Masterform geerbt wurde.
### **Programmierbeispiel für Stamminformationen abrufen**
Der folgende Codeabschnitt ruft die Masterinformationen von diagram ab.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-RetrieveMasterInfo-RetrieveMasterInfo.cs" >}}
## **Fügen Sie Master aus der Schablone der Formen hinzu**
Eine Schablone ist eine Sammlung von Formen, die einer bestimmten Microsoft Office Visio Vorlage zugeordnet sind. Mit Aspose.Diagram ist es möglich, beliebige Shape-Master zu einer Zeichnung aus einer Schablone hinzuzufügen.
### **Meister hinzufügen**
 Das[Meister](http://www.aspose.com/api/net/diagram/aspose.diagram/master) Objekt repräsentiert a[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Master des Objekts in einem diagram. Die Methode AddMaster, die von der Klasse Diagram verfügbar gemacht wird, ermöglicht das Hinzufügen eines Masters aus einer Schablone. Es bietet die folgenden vier Möglichkeiten:

- Pfad der Schablonendatei und Master-ID.
- Dateipfad und Mastername der Schablone.
- Schablonendateistream und Master-ID.
- Schablonendateistream und Mastername.
- Master zu diagram aus Quelle diagram hinzufügen
#### **Master-Programmierbeispiel hinzufügen**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-AddMasterFromStencil-AddMasterFromStencil.cs" >}}
## **Master von Grund auf neu erstellen**
 Aspose.Diagram API ermöglicht das Erstellen einer[Meister](http://www.aspose.com/api/net/diagram/aspose.diagram/master) von Grund auf ohne Schablone, Zeichnung oder Vorlage. Entwickler können die Erstellung von Master anpassen. Die Methode AddMaster, die von der Klasse Diagram verfügbar gemacht wird, ermöglicht das Hinzufügen eines Masters.
### **Master-Programmierbeispiel erstellen**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateMasterFromScratch-CreateMasterFromScratch.cs" >}}
## **Holen Sie sich einen Master aus der Datei Visio**
Manchmal müssen Entwickler die Details des Masters einer Visio-Zeichnung abrufen. Die Aspose.Diagram API unterstützt diese Funktion.

 Aspose.Diagram for .NET bietet die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Klasse, die eine Visio-Zeichnung darstellt. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um die Details eines bestimmten Masters abzurufen. Die Klasse MasterCollection macht die Methoden GetMasterByName und GetMaster verfügbar, die aufgerufen werden können, um ein Master-Objekt abzurufen.
### **Abrufen eines Master-Objekts nach ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetMaster-Methode der Diagram.Masters-Klasse auf.
#### **Programmierbeispiel für Master-Objekt nach ID**
Das folgende Beispiel zeigt, wie Sie einen Master nach ID aus einer Visio-Zeichnung erhalten.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyID-GetMasterbyID.cs" >}}
### **Abrufen eines Master-Objekts nach Namen**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetMasterByName-Methode der Diagram.Masters-Klasse auf.
#### **Master Object by Name Programmierbeispiel**
Das folgende Beispiel zeigt, wie Sie ein Master-Objekt anhand des Namens aus einer Visio-Zeichnung abrufen.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyName-GetMasterbyName.cs" >}}
## **Überprüfen Sie das Vorhandensein eines Masters in der Visio-Zeichnung**
Die Aspose.Diagram API unterstützt die Überprüfung auf das Vorhandensein eines Masters in einer Visio-Zeichnung. Mit der MasterCollection-Eigenschaft können Entwickler anhand ihres Namens oder ihrer ID prüfen, ob ein Master vorhanden ist.

 Aspose.Diagram for .NET bietet die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Die Masters-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Master-Objekten. Diese Eigenschaft kann verwendet werden, um das Vorhandensein eines bestimmten Masters zu überprüfen. Die MasterCollection-Klasse macht die IsExist-Methode verfügbar, die mit dem Masternamen- oder ID-Parameter aufgerufen werden kann.
### **Überprüfen einer Master-Anwesenheit anhand der ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die IsExist-Methode der Diagram.Masters-Klasse auf.
#### **Master Presence by ID Programmierbeispiel**
Das folgende Beispiel zeigt, wie das Vorhandensein eines Masters anhand der ID in einer Visio-Zeichnung überprüft wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.cs" >}}
### **Überprüfen einer Master-Anwesenheit anhand des Namens**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die IsExist-Methode der Diagram.Masters-Klasse auf.
#### **Master Presence by Name Programmierbeispiel**
Das folgende Beispiel zeigt, wie eine Master-Anwesenheit anhand des Namens aus der Zeichnung Visio überprüft wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.cs" >}}
