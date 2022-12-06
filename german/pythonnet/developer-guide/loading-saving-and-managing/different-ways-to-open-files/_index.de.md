---
title: Verschiedene Möglichkeiten zum Öffnen von Dateien
type: docs
weight: 10
url: /de/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Mit Aspose.Diagram ist es beispielsweise einfach, Dateien zu öffnen, Daten abzurufen oder eine Designer-Vorlage zu verwenden, um den Entwicklungsprozess zu beschleunigen.

{{% /alert %}}

## **Öffnen einer Datei über einen Pfad**

 Entwickler können eine Microsoft Diagram-Datei öffnen, indem sie ihren Dateipfad auf dem lokalen Computer verwenden, indem sie ihn in der**Diagram**Klassenkonstrukteur. Übergeben Sie den Pfad einfach im Konstruktor als a*Schnur*. Aspose.Diagram erkennt automatisch den Dateiformattyp.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **Öffnen einer Datei über einen Stream**

 Es ist auch einfach, eine Visio-Datei als Stream zu öffnen. Verwenden Sie dazu eine überladene Version des Konstruktors, der die akzeptiert*BufferStream*Objekt, das die Datei enthält.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **Öffnen einer Datei mit LoadOptions**

 Um eine Datei mit Ladeoptionen zu öffnen, verwenden Sie die**Ladeoptionen**Klassen, um die zugehörigen Optionen der Klassen für die zu ladende Vorlagendatei festzulegen.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

