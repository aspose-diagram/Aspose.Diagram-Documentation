---
title: Utilizzo di origini dati esterne
type: docs
weight: 190
url: /it/java/working-with-external-data-sources/
---
## **Aggiornamento Connessione Dati del Disegno Visio**
Aspose.Diagram API consente agli utenti di modificare la connessione dati di SQL Server del disegno Visio collegato. Per inserire i dati nel disegno Visio, è necessario accedere ai dati di SQL Server. Assicurarsi che il database non sia aperto in modalità esclusiva.

 Ora è un fenomeno comune collegare i dati dei diagrammi Microsoft Visio dalle fonti di dati esterne. Il[DataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) class contiene tutte le connessioni dati.
### **Esempio di programmazione**
La parte di codice seguente modifica una particolare connessione dati e aggiorna anche tutti i set di record disponibili in Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-ExternalDataSources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.java" >}}
