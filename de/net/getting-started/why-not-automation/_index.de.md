---
title: Warum nicht Automatisierung
type: docs
weight: 40
url: /de/net/why-not-automation/
description: Diese Seite beschreibt, warum keine Automatisierung.
---
{{% alert color="primary" %}} 

Warum sind Aspose-Komponenten eine viel bessere Option als Microsoft Office-Automatisierung?*

Zwei Fragen hören wir hier unter Aspose am häufigsten:

1. **Benötigen Ihre Produkte die Installation von Microsoft Office, damit sie ausgeführt werden können?** 
Die einfache Antwort ist nein. Aspose-Komponenten sind völlig unabhängig und weder mit der Microsoft Corporation verbunden noch autorisiert, gesponsert oder anderweitig genehmigt.
1. **Warum sollten wir Aspose-Produkte verwenden, anstatt Microsoft Office-Automatisierung zu nutzen?** 
 Die kürzeste Antwort, die wir geben könnten, ist, dass es viele Gründe gibt, wobei der Hauptgrund darin besteht, dass Microsoft selbst dringend von der Office-Automatisierung durch Softwarelösungen abrät:[Überlegungen zur serverseitigen Automatisierung von Office](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q257757).

{{% /alert %}} 
## **Warum nicht Automatisierung**
Es gibt mehrere Gründe, warum Aspose-Komponenten eine bessere Alternative zur Automatisierung sind. Einige der wichtigsten Punkte werden im Folgenden beschrieben. Besuchen Sie auch unbedingt die Links am Ende dieses Abschnitts.
### **Sicherheit**
Das Folgende ist ein direktes Zitat aus dem oben genannten Artikel Microsoft:

*"Office Anwendungen waren nie für die serverseitige Verwendung vorgesehen und berücksichtigen daher nicht die Sicherheitsprobleme, mit denen verteilte Komponenten konfrontiert sind. Office authentifiziert keine eingehenden Anforderungen und schützt Sie nicht vor dem unbeabsichtigten Ausführen von Makros oder dem Starten eines anderen Servers die Makros ausführen könnten, aus Ihrem serverseitigen Code. Öffnen Sie keine Dateien, die von einem anonymen Web auf den Server hochgeladen werden! Basierend auf den zuletzt festgelegten Sicherheitseinstellungen kann der Server Makros unter einem Administrator- oder Systemkontext mit vollständig ausführen Privilegien und gefährden Ihr Netzwerk!Außerdem verwendet Office viele Client-seitige Komponenten (wie Simple MAPI, WinInet und MSDAIPP), die Client-Authentifizierungsinformationen zwischenspeichern können, um die Verarbeitung zu beschleunigen.Wenn Office serverseitig automatisiert wird, eine Eine Instanz kann mehr als einen Client bedienen, und da Authentifizierungsinformationen für diese Sitzung zwischengespeichert wurden, ist es möglich, dass ein Client den Cache verwenden kann Zugangsdaten eines anderen Clients ausgeben und dadurch nicht gewährte Zugriffsberechtigungen erhalten, indem Sie sich als andere Benutzer ausgeben."*

Aspose Produkte sind sehr sicher. Aspose-Komponenten werden im selben Benutzerkontext wie alle ASP.NET-Anwendungen unter dem ASPNET-Benutzer ausgeführt. Daher stellen Aspose-Komponenten kein potenzielles Risiko für wichtige Systemressourcen dar. Außerdem werden Makros nicht automatisch ausgeführt, wenn ein Dokument von einer Aspose-Komponente geöffnet wird. Aspose-Komponenten wurden mit dem Ziel entwickelt, Entwicklern das Erstellen, Bearbeiten und Speichern von Office-Dateien zu ermöglichen. Keines der mit dem Paket Microsoft Office verbundenen Risiken ist den Komponenten von Aspose eigen.
### **Stabilität**
Das Folgende ist ein direktes Zitat aus dem oben genannten Artikel Microsoft:

*"Office 2000, Office XP und Office 2003 verwenden die Microsoft Windows Installer (MSI)-Technologie, um die Installation und Selbstreparatur für Endbenutzer zu vereinfachen. MSI führt das Konzept der "Installation bei der ersten Verwendung" ein, das die dynamische Installation von Funktionen ermöglicht oder zur Laufzeit konfiguriert (für das System oder häufiger für einen bestimmten Benutzer) In einer serverseitigen Umgebung verlangsamt dies sowohl die Leistung als auch die Wahrscheinlichkeit, dass ein Dialogfeld angezeigt wird, in dem der Benutzer aufgefordert wird, die Installation zu genehmigen oder bereitzustellen eine geeignete Installationsdiskette. Obwohl es darauf ausgelegt ist, die Widerstandsfähigkeit von Office als Endbenutzerprodukt zu erhöhen, ist die Implementierung von MSI-Funktionen in Office in einer serverseitigen Umgebung kontraproduktiv. Darüber hinaus kann die Stabilität von Office im Allgemeinen nicht gewährleistet werden, wenn ein Server ausgeführt wird -side, da es nicht für diese Art der Verwendung entwickelt oder getestet wurde.Die Verwendung von Office als Dienstkomponente auf einem Netzwerkserver kann die Stabilität dieses Computers und als verringern eine Folge Ihr Netzwerk als Ganzes. Wenn Sie planen, Office serverseitig zu automatisieren, versuchen Sie, das Programm auf einem dedizierten Computer zu isolieren, der keine kritischen Funktionen beeinträchtigen kann und der bei Bedarf neu gestartet werden kann."*

Da Aspose-Komponenten in einer einzigen DLL gepackt sind, müssen keine zusätzlichen Teile oder Teile installiert werden, damit sie funktionieren. Aspose-Komponenten werden nur von .NET-Anwendungen verwendet, und es gibt keinen Teil des Komponentencodes, der darauf ausgelegt ist, auf eine menschliche Antwort zu warten. Aspose Komponenten wurden ausgiebig getestet. Aspose-Komponenten werden von Unternehmen wie IBM, Hilton, Reader's Digest, Bank of America und vielen mehr verwendet.
### **Skalierbarkeit/Geschwindigkeit**
Das Folgende ist ein direktes Zitat aus dem oben genannten Artikel Microsoft:

*„Serverseitige Komponenten müssen hochgradig ablaufinvariante Multithread-COM-Komponenten mit minimalem Overhead und hohem Durchsatz für mehrere Clients sein entwickelt, um vielfältige, aber ressourcenintensive Funktionalität für einen einzelnen Client bereitzustellen. Sie bieten wenig Skalierbarkeit als serverseitige Lösung und haben feste Grenzen für wichtige Elemente wie Speicher, die nicht durch Konfiguration geändert werden können. Noch wichtiger ist, dass sie global verwenden Ressourcen (z. B. speicherabgebildete Dateien, globale Add-Ins oder Vorlagen und gemeinsam genutzte Automatisierungsserver), die die Anzahl der Instanzen begrenzen können, die gleichzeitig ausgeführt werden können, und zu Wettlaufbedingungen führen können, wenn sie in einer Umgebung mit mehreren Clients konfiguriert sind Planen, mehr als eine Instanz einer Office-Anwendung gleichzeitig auszuführen, müssen Sie den Zugriff auf die Office-Anwendung "poolen" oder serialisieren, um Pote zu vermeiden tielle Deadlocks oder Datenkorruption."*

Aspose-Komponenten sind hochgradig skalierbar und blitzschnell. Office-Anwendungen wurden nicht dafür entwickelt, von Hunderten und Tausenden von Benutzern gleichzeitig verwendet zu werden; Aspose-Komponenten sind jedoch genau dafür ausgelegt. Unsere Komponenten sind eine echte .NET-Lösung und funktionieren einwandfrei, egal ob auf einem einzelnen Server, der eine einzelne Anwendung betreibt, oder auf einer Webfarm mit Lastausgleich, die eine unternehmensweite Anwendung betreibt.
### **Preis**
 Wenn eine Anwendung Microsoft Office-Automatisierung verwendet, muss eine Kopie von Microsoft Office für jeden Computer erworben werden, auf dem die Anwendung ausgeführt wird. Es kommt oft vor, dass eine Anwendung eine office-Datei erstellen oder bearbeiten muss, der Benutzer jedoch nicht über Office verfügen muss. Aspose bietet eine sehr gute[kosteneffizient](https://purchase.aspose.com/buy), gebührenfreie Weiterverteilungslizenz, die eine Bereitstellung für eine unbegrenzte Anzahl von Benutzern ohne Lizenzsorgen ermöglicht.

Bei der Erstellung webbasierter Anwendungen ist es wichtig zu wissen, dass Microsoft Office Automatisierungskomponenten für serverseitige Lösungen weder preislich noch lizenziert sind ([Lizenzierung der Office 2000 Web Components und Office Server Extensions](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q243006)); Daher gibt es keine gute Lizenzierungslösung für die Bereitstellung von Webanwendungen, die die Microsoft Office-Komponenten verwenden. Aspose bietet auch für serverbasierte Anwendungen eine sehr kostengünstige Lösung.
### **Merkmale**
 Aspose-Komponenten bieten alles, was zum Verwalten von Office-Dateien benötigt wird, und vieles mehr. Sie wurden mit der Philosophie entwickelt, Entwicklern zu ermöglichen, mit dem geringsten Arbeitsaufwand die besten Ergebnisse zu erzielen. Im Gegensatz zur Office-Automatisierung bieten die Aspose-Komponenten viele leistungsstarke, zeitsparende Funktionen. Zum Beispiel,[Aspose.Diagram](https://products.aspose.com/diagram/net/) bietet Entwicklern die Möglichkeit, Visio diagram und seine Formen zu erstellen, zu lesen, zu schreiben, zu exportieren, zu drucken, darauf zuzugreifen und sie zu schützen.[Jede Komponente](https://products.aspose.com/total/) in der Aspose-Familie bieten ihre eigenen einzigartigen, leistungsstarken Funktionen.

Das Beste am Kauf einer Aspose-Komponente oder einer Komponentensuite ist der Zugang zu unseren Entwicklungsteams. Unsere Entwicklungsteams wissen, dass, wenn es eine Funktion gibt, die Ihr Unternehmen benötigt, höchstwahrscheinlich auch andere Unternehmen diese benötigen werden. Obwohl nicht jede Funktionsanfrage hinzugefügt werden kann, versuchen unsere Teams, bei der Bereitstellung von Unterstützung sehr aufgeschlossen und flexibel zu sein. Diese Denkweise hat Aspose-Komponenten geholfen, so leistungsfähig zu werden, wie sie sind. Wenn Sie zusätzliche Funktionen von Office-Automatisierungsobjekten benötigen, sind Ihre Chancen, dass sie hinzugefügt werden, sehr, sehr gering.
### **Fazit**
{{% alert color="primary" %}} 

 Während dieser Artikel viele der wichtigsten Punkte behandelt hat, warum Aspose-Komponenten eine bessere Wahl sind als Office-Automatisierung, gibt es noch viele, viele mehr. Dieser Artikel behandelt hauptsächlich nur die wichtigsten Punkte. Alle der verschiedenen Aspose-Komponenten bieten ein risikofreies, unverbindliches Angebot[Testversion](https://www.nuget.org/packages/Aspose.Diagram/)Wir empfehlen Ihnen, diese Bewertung zu nutzen, um besser zu sehen, was Aspose für Ihre Bewerbungen tun kann.

{{% /alert %}}
